---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 84cc6f2e8e51de6176b4ab8a04296aab8516a967
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989476"
---
# <span data-ttu-id="f0c31-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="f0c31-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="f0c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0c31-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c31-103">Ottiene un elenco delle posizioni dei servizi di peering offerte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f0c31-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="f0c31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0c31-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0c31-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0c31-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c31-106">Elencare le posizioni di peering.</span><span class="sxs-lookup"><span data-stu-id="f0c31-106">List peering locations.</span></span>

## <span data-ttu-id="f0c31-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0c31-107">EXAMPLES</span></span>

### <span data-ttu-id="f0c31-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f0c31-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="f0c31-109">Recupera le posizioni di peering per Washington.</span><span class="sxs-lookup"><span data-stu-id="f0c31-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="f0c31-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f0c31-110">Example 2</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States"

Country     : United States
State       : Alabama
AzureRegion : East US
Name        : Alabama
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

Country     : United States
State       : Arizona
AzureRegion : West US
Name        : Arizona
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

...
```

<span data-ttu-id="f0c31-111">Recupera le posizioni di peering per Washington.</span><span class="sxs-lookup"><span data-stu-id="f0c31-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="f0c31-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0c31-112">PARAMETERS</span></span>

### <span data-ttu-id="f0c31-113">-Paese</span><span class="sxs-lookup"><span data-stu-id="f0c31-113">-Country</span></span>
<span data-ttu-id="f0c31-114">Filtro paese</span><span class="sxs-lookup"><span data-stu-id="f0c31-114">The country filter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c31-115">-DefaultProfile</span></span>
<span data-ttu-id="f0c31-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0c31-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c31-117">CommonParameters</span></span>
<span data-ttu-id="f0c31-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c31-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c31-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f0c31-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c31-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0c31-120">INPUTS</span></span>

### <span data-ttu-id="f0c31-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f0c31-121">None</span></span>

## <span data-ttu-id="f0c31-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0c31-122">OUTPUTS</span></span>

### <span data-ttu-id="f0c31-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSZionamentoingServiceLocation</span><span class="sxs-lookup"><span data-stu-id="f0c31-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="f0c31-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0c31-124">NOTES</span></span>

## <span data-ttu-id="f0c31-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0c31-125">RELATED LINKS</span></span>
