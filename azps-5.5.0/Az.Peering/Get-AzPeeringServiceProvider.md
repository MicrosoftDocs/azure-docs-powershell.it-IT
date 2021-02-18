---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202279"
---
# <span data-ttu-id="6f06f-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="6f06f-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="6f06f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f06f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f06f-103">Ottiene un elenco di provider di servizi di peering in collaborazione con Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6f06f-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="6f06f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f06f-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f06f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6f06f-105">DESCRIPTION</span></span>
<span data-ttu-id="6f06f-106">Elencare i provider di servizi di peering</span><span class="sxs-lookup"><span data-stu-id="6f06f-106">List peering service providers</span></span>

## <span data-ttu-id="6f06f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f06f-107">EXAMPLES</span></span>

### <span data-ttu-id="6f06f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6f06f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="6f06f-109">Ottiene i provider di servizi di peering disponibili</span><span class="sxs-lookup"><span data-stu-id="6f06f-109">Gets available peering service providers</span></span>

## <span data-ttu-id="6f06f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f06f-110">PARAMETERS</span></span>

### <span data-ttu-id="6f06f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f06f-111">-DefaultProfile</span></span>
<span data-ttu-id="6f06f-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f06f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f06f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f06f-113">CommonParameters</span></span>
<span data-ttu-id="6f06f-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f06f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f06f-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6f06f-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f06f-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="6f06f-116">INPUTS</span></span>

### <span data-ttu-id="6f06f-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6f06f-117">None</span></span>

## <span data-ttu-id="6f06f-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f06f-118">OUTPUTS</span></span>

### <span data-ttu-id="6f06f-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioningServiceProvider</span><span class="sxs-lookup"><span data-stu-id="6f06f-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="6f06f-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="6f06f-120">NOTES</span></span>

## <span data-ttu-id="6f06f-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f06f-121">RELATED LINKS</span></span>
