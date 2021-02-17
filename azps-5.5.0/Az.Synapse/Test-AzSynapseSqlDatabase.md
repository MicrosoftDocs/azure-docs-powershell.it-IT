---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207587"
---
# <span data-ttu-id="38743-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="38743-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="38743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38743-102">SYNOPSIS</span></span>
<span data-ttu-id="38743-103">Verifica la presenza di un database synapse Analytics SQL database.</span><span class="sxs-lookup"><span data-stu-id="38743-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="38743-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38743-104">SYNTAX</span></span>

### <span data-ttu-id="38743-105">TestByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38743-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38743-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38743-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38743-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38743-107">DESCRIPTION</span></span>
<span data-ttu-id="38743-108">Il cmdlet **Test-AzSynapseSqlDatabase** verifica l'esistenza di un database di SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="38743-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="38743-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38743-109">EXAMPLES</span></span>

### <span data-ttu-id="38743-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38743-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="38743-111">Questo comando verifica l'esistenza della cartella di SQL database.</span><span class="sxs-lookup"><span data-stu-id="38743-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="38743-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38743-112">PARAMETERS</span></span>

### <span data-ttu-id="38743-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38743-113">-DefaultProfile</span></span>
<span data-ttu-id="38743-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38743-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38743-115">-Name</span><span class="sxs-lookup"><span data-stu-id="38743-115">-Name</span></span>
<span data-ttu-id="38743-116">Nome dell'account synapse SQL Database.</span><span class="sxs-lookup"><span data-stu-id="38743-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="38743-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38743-117">-ResourceGroupName</span></span>
<span data-ttu-id="38743-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38743-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38743-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="38743-119">-WorkspaceName</span></span>
<span data-ttu-id="38743-120">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="38743-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38743-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="38743-121">-WorkspaceObject</span></span>
<span data-ttu-id="38743-122">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="38743-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38743-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38743-123">CommonParameters</span></span>
<span data-ttu-id="38743-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38743-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38743-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38743-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38743-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="38743-126">INPUTS</span></span>

### <span data-ttu-id="38743-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="38743-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="38743-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38743-128">OUTPUTS</span></span>

### <span data-ttu-id="38743-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38743-129">System.Boolean</span></span>

## <span data-ttu-id="38743-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="38743-130">NOTES</span></span>

## <span data-ttu-id="38743-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38743-131">RELATED LINKS</span></span>
