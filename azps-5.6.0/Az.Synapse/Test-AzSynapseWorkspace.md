---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: e92b4d20e89df451c483bc0b4bdccb83fdc8a140
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011198"
---
# <span data-ttu-id="06113-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="06113-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="06113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06113-102">SYNOPSIS</span></span>
<span data-ttu-id="06113-103">Verifica la presenza di un'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="06113-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="06113-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06113-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06113-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="06113-105">DESCRIPTION</span></span>
<span data-ttu-id="06113-106">Il cmdlet **Test-AzSynapseWorkspace** verifica l'esistenza di un'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="06113-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="06113-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06113-107">EXAMPLES</span></span>

### <span data-ttu-id="06113-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06113-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="06113-109">Questo comando verifica l'esistenza di un'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="06113-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="06113-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06113-110">PARAMETERS</span></span>

### <span data-ttu-id="06113-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06113-111">-DefaultProfile</span></span>
<span data-ttu-id="06113-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06113-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06113-113">-Name</span><span class="sxs-lookup"><span data-stu-id="06113-113">-Name</span></span>
<span data-ttu-id="06113-114">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="06113-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="06113-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06113-115">-ResourceGroupName</span></span>
<span data-ttu-id="06113-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06113-116">Resource group name.</span></span>

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

### <span data-ttu-id="06113-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06113-117">CommonParameters</span></span>
<span data-ttu-id="06113-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06113-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06113-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="06113-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06113-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="06113-120">INPUTS</span></span>

### <span data-ttu-id="06113-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="06113-121">None</span></span>

## <span data-ttu-id="06113-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06113-122">OUTPUTS</span></span>

### <span data-ttu-id="06113-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="06113-123">System.Object</span></span>
## <span data-ttu-id="06113-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="06113-124">NOTES</span></span>

## <span data-ttu-id="06113-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06113-125">RELATED LINKS</span></span>
