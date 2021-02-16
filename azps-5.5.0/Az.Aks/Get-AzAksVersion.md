---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199863"
---
# <span data-ttu-id="c5863-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="c5863-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="c5863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5863-102">SYNOPSIS</span></span>
<span data-ttu-id="c5863-103">Elencare la versione disponibile per la creazione del cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="c5863-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c5863-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5863-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5863-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c5863-105">DESCRIPTION</span></span>
<span data-ttu-id="c5863-106">Elencare la versione disponibile per la creazione del cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="c5863-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c5863-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5863-107">EXAMPLES</span></span>

### <span data-ttu-id="c5863-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5863-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="c5863-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5863-109">PARAMETERS</span></span>

### <span data-ttu-id="c5863-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5863-110">-DefaultProfile</span></span>
<span data-ttu-id="c5863-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5863-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5863-112">-Location</span><span class="sxs-lookup"><span data-stu-id="c5863-112">-Location</span></span>
<span data-ttu-id="c5863-113">Posizione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="c5863-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="c5863-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5863-114">CommonParameters</span></span>
<span data-ttu-id="c5863-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5863-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5863-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5863-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5863-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="c5863-117">INPUTS</span></span>

### <span data-ttu-id="c5863-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c5863-118">None</span></span>

## <span data-ttu-id="c5863-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5863-119">OUTPUTS</span></span>

### <span data-ttu-id="c5863-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="c5863-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="c5863-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="c5863-121">NOTES</span></span>

## <span data-ttu-id="c5863-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5863-122">RELATED LINKS</span></span>
