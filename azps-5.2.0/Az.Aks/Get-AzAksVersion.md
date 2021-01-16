---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356509"
---
# <span data-ttu-id="cbbe9-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="cbbe9-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="cbbe9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cbbe9-102">SYNOPSIS</span></span>
<span data-ttu-id="cbbe9-103">Elencare la versione disponibile per la creazione di cluster Kubernetes gestiti.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="cbbe9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbbe9-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbbe9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbbe9-105">DESCRIPTION</span></span>
<span data-ttu-id="cbbe9-106">Elencare la versione disponibile per la creazione di cluster Kubernetes gestiti.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="cbbe9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbbe9-107">EXAMPLES</span></span>

### <span data-ttu-id="cbbe9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cbbe9-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="cbbe9-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cbbe9-109">PARAMETERS</span></span>

### <span data-ttu-id="cbbe9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbbe9-110">-DefaultProfile</span></span>
<span data-ttu-id="cbbe9-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbbe9-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cbbe9-112">-Location</span></span>
<span data-ttu-id="cbbe9-113">Posizione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="cbbe9-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbbe9-114">CommonParameters</span></span>
<span data-ttu-id="cbbe9-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbbe9-116">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbbe9-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbbe9-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cbbe9-117">INPUTS</span></span>

### <span data-ttu-id="cbbe9-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cbbe9-118">None</span></span>

## <span data-ttu-id="cbbe9-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbbe9-119">OUTPUTS</span></span>

### <span data-ttu-id="cbbe9-120">Microsoft. Azure. Commands. AKS. Models. PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="cbbe9-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="cbbe9-121">Note</span><span class="sxs-lookup"><span data-stu-id="cbbe9-121">NOTES</span></span>

## <span data-ttu-id="cbbe9-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbbe9-122">RELATED LINKS</span></span>
