---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384845"
---
# <span data-ttu-id="ff9e3-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ff9e3-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="ff9e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff9e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9e3-103">Ottiene un elenco dei provider di servizi peer che hanno collaborato con Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="ff9e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff9e3-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff9e3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff9e3-105">DESCRIPTION</span></span>
<span data-ttu-id="ff9e3-106">Provider di servizi di peering elenco</span><span class="sxs-lookup"><span data-stu-id="ff9e3-106">List peering service providers</span></span>

## <span data-ttu-id="ff9e3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff9e3-107">EXAMPLES</span></span>

### <span data-ttu-id="ff9e3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ff9e3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="ff9e3-109">Ottiene i provider di servizi peering disponibili</span><span class="sxs-lookup"><span data-stu-id="ff9e3-109">Gets available peering service providers</span></span>

## <span data-ttu-id="ff9e3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff9e3-110">PARAMETERS</span></span>

### <span data-ttu-id="ff9e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9e3-111">-DefaultProfile</span></span>
<span data-ttu-id="ff9e3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff9e3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9e3-113">CommonParameters</span></span>
<span data-ttu-id="ff9e3-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9e3-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff9e3-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9e3-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff9e3-116">INPUTS</span></span>

### <span data-ttu-id="ff9e3-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ff9e3-117">None</span></span>

## <span data-ttu-id="ff9e3-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff9e3-118">OUTPUTS</span></span>

### <span data-ttu-id="ff9e3-119">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ff9e3-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="ff9e3-120">Note</span><span class="sxs-lookup"><span data-stu-id="ff9e3-120">NOTES</span></span>

## <span data-ttu-id="ff9e3-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff9e3-121">RELATED LINKS</span></span>
