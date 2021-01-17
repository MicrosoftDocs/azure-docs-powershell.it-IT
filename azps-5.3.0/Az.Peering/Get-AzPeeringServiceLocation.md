---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384873"
---
# <span data-ttu-id="2e340-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="2e340-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="2e340-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e340-102">SYNOPSIS</span></span>
<span data-ttu-id="2e340-103">Ottiene un elenco dei percorsi di servizio peer offerti da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2e340-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="2e340-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e340-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e340-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e340-105">DESCRIPTION</span></span>
<span data-ttu-id="2e340-106">Elencare le posizioni di peering.</span><span class="sxs-lookup"><span data-stu-id="2e340-106">List peering locations.</span></span>

## <span data-ttu-id="2e340-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e340-107">EXAMPLES</span></span>

### <span data-ttu-id="2e340-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2e340-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="2e340-109">Recupera le posizioni di peering per Washington.</span><span class="sxs-lookup"><span data-stu-id="2e340-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="2e340-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2e340-110">Example 2</span></span>
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

<span data-ttu-id="2e340-111">Recupera le posizioni di peering per Washington.</span><span class="sxs-lookup"><span data-stu-id="2e340-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="2e340-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e340-112">PARAMETERS</span></span>

### <span data-ttu-id="2e340-113">-Paese</span><span class="sxs-lookup"><span data-stu-id="2e340-113">-Country</span></span>
<span data-ttu-id="2e340-114">Filtro paese</span><span class="sxs-lookup"><span data-stu-id="2e340-114">The country filter</span></span>

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

### <span data-ttu-id="2e340-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e340-115">-DefaultProfile</span></span>
<span data-ttu-id="2e340-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e340-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e340-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e340-117">CommonParameters</span></span>
<span data-ttu-id="2e340-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e340-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e340-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e340-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e340-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e340-120">INPUTS</span></span>

### <span data-ttu-id="2e340-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2e340-121">None</span></span>

## <span data-ttu-id="2e340-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e340-122">OUTPUTS</span></span>

### <span data-ttu-id="2e340-123">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="2e340-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="2e340-124">Note</span><span class="sxs-lookup"><span data-stu-id="2e340-124">NOTES</span></span>

## <span data-ttu-id="2e340-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e340-125">RELATED LINKS</span></span>
