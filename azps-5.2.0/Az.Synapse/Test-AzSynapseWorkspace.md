---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339820"
---
# <span data-ttu-id="a16d7-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a16d7-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="a16d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a16d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a16d7-103">Verifica l'esistenza di un'area di lavoro di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a16d7-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="a16d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a16d7-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a16d7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a16d7-105">DESCRIPTION</span></span>
<span data-ttu-id="a16d7-106">Il cmdlet **test-AzSynapseWorkspace** controlla l'esistenza di un'area di lavoro di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a16d7-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="a16d7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a16d7-107">EXAMPLES</span></span>

### <span data-ttu-id="a16d7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a16d7-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="a16d7-109">Questo comando controlla l'esistenza di un'area di lavoro di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a16d7-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="a16d7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a16d7-110">PARAMETERS</span></span>

### <span data-ttu-id="a16d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16d7-111">-DefaultProfile</span></span>
<span data-ttu-id="a16d7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a16d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a16d7-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a16d7-113">-Name</span></span>
<span data-ttu-id="a16d7-114">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a16d7-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a16d7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a16d7-115">-ResourceGroupName</span></span>
<span data-ttu-id="a16d7-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a16d7-116">Resource group name.</span></span>

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

### <span data-ttu-id="a16d7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16d7-117">CommonParameters</span></span>
<span data-ttu-id="a16d7-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a16d7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16d7-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a16d7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16d7-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a16d7-120">INPUTS</span></span>

### <span data-ttu-id="a16d7-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a16d7-121">None</span></span>

## <span data-ttu-id="a16d7-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a16d7-122">OUTPUTS</span></span>

### <span data-ttu-id="a16d7-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="a16d7-123">System.Object</span></span>
## <span data-ttu-id="a16d7-124">Note</span><span class="sxs-lookup"><span data-stu-id="a16d7-124">NOTES</span></span>

## <span data-ttu-id="a16d7-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a16d7-125">RELATED LINKS</span></span>
