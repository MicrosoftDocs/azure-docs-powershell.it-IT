---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207586"
---
# <span data-ttu-id="7da1d-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7da1d-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="7da1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7da1d-102">SYNOPSIS</span></span>
<span data-ttu-id="7da1d-103">Verifica la presenza di un'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7da1d-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="7da1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7da1d-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7da1d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7da1d-105">DESCRIPTION</span></span>
<span data-ttu-id="7da1d-106">Il cmdlet **Test-AzSynapseWorkspace** verifica l'esistenza di un'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7da1d-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="7da1d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7da1d-107">EXAMPLES</span></span>

### <span data-ttu-id="7da1d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7da1d-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="7da1d-109">Questo comando verifica l'esistenza di un'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7da1d-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="7da1d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7da1d-110">PARAMETERS</span></span>

### <span data-ttu-id="7da1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da1d-111">-DefaultProfile</span></span>
<span data-ttu-id="7da1d-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7da1d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7da1d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7da1d-113">-Name</span></span>
<span data-ttu-id="7da1d-114">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="7da1d-114">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7da1d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da1d-115">-ResourceGroupName</span></span>
<span data-ttu-id="7da1d-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7da1d-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7da1d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da1d-117">CommonParameters</span></span>
<span data-ttu-id="7da1d-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da1d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da1d-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7da1d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da1d-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="7da1d-120">INPUTS</span></span>

### <span data-ttu-id="7da1d-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7da1d-121">None</span></span>

## <span data-ttu-id="7da1d-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7da1d-122">OUTPUTS</span></span>

### <span data-ttu-id="7da1d-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="7da1d-123">System.Object</span></span>
## <span data-ttu-id="7da1d-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="7da1d-124">NOTES</span></span>

## <span data-ttu-id="7da1d-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7da1d-125">RELATED LINKS</span></span>
