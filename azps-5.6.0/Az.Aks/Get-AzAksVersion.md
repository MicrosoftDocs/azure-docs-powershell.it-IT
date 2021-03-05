---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 3a46f28ad0f169f4f4f280922dff675b5e749fed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966894"
---
# <span data-ttu-id="c0a8f-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="c0a8f-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="c0a8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a8f-103">Elencare la versione disponibile per la creazione del cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c0a8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0a8f-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0a8f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c0a8f-105">DESCRIPTION</span></span>
<span data-ttu-id="c0a8f-106">Elencare la versione disponibile per la creazione del cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c0a8f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0a8f-107">EXAMPLES</span></span>

### <span data-ttu-id="c0a8f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0a8f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="c0a8f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0a8f-109">PARAMETERS</span></span>

### <span data-ttu-id="c0a8f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a8f-110">-DefaultProfile</span></span>
<span data-ttu-id="c0a8f-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0a8f-112">-Location</span><span class="sxs-lookup"><span data-stu-id="c0a8f-112">-Location</span></span>
<span data-ttu-id="c0a8f-113">Posizione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="c0a8f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a8f-114">CommonParameters</span></span>
<span data-ttu-id="c0a8f-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a8f-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a8f-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="c0a8f-117">INPUTS</span></span>

### <span data-ttu-id="c0a8f-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c0a8f-118">None</span></span>

## <span data-ttu-id="c0a8f-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0a8f-119">OUTPUTS</span></span>

### <span data-ttu-id="c0a8f-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="c0a8f-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="c0a8f-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="c0a8f-121">NOTES</span></span>

## <span data-ttu-id="c0a8f-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0a8f-122">RELATED LINKS</span></span>
