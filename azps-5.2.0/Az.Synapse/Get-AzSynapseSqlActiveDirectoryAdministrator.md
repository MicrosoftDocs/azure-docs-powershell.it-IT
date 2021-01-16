---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334072"
---
# <span data-ttu-id="b0171-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b0171-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="b0171-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0171-102">SYNOPSIS</span></span>
<span data-ttu-id="b0171-103">Ottiene informazioni su un amministratore di Azure AD per l'area di lavoro di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b0171-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="b0171-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0171-104">SYNTAX</span></span>

### <span data-ttu-id="b0171-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0171-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0171-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0171-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0171-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0171-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0171-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0171-108">DESCRIPTION</span></span>
<span data-ttu-id="b0171-109">Il cmdlet **Get-AzSynapseSqlActiveDirectoryAdministrator** ottiene le informazioni su un amministratore di Azure Active Directory (Azure ad) per un'area di lavoro di analisi di Azure sinapsi nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b0171-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="b0171-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0171-110">EXAMPLES</span></span>

### <span data-ttu-id="b0171-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0171-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b0171-112">Questo comando consente di ottenere informazioni su un amministratore di Azure AD per un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b0171-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="b0171-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0171-113">PARAMETERS</span></span>

### <span data-ttu-id="b0171-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0171-114">-DefaultProfile</span></span>
<span data-ttu-id="b0171-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0171-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0171-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0171-116">-InputObject</span></span>
<span data-ttu-id="b0171-117">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0171-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b0171-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0171-118">-ResourceGroupName</span></span>
<span data-ttu-id="b0171-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0171-119">Resource group name.</span></span>

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

### <span data-ttu-id="b0171-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0171-120">-ResourceId</span></span>
<span data-ttu-id="b0171-121">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b0171-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="b0171-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b0171-122">-WorkspaceName</span></span>
<span data-ttu-id="b0171-123">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b0171-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b0171-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0171-124">CommonParameters</span></span>
<span data-ttu-id="b0171-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0171-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0171-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0171-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0171-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0171-127">INPUTS</span></span>

### <span data-ttu-id="b0171-128">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b0171-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b0171-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0171-129">OUTPUTS</span></span>

### <span data-ttu-id="b0171-130">Microsoft. Azure. Commands. sinapsi. Models. PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="b0171-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="b0171-131">Note</span><span class="sxs-lookup"><span data-stu-id="b0171-131">NOTES</span></span>

## <span data-ttu-id="b0171-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0171-132">RELATED LINKS</span></span>
