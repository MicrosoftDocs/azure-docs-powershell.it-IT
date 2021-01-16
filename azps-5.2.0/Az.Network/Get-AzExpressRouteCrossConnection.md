---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331276"
---
# <span data-ttu-id="49615-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="49615-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="49615-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49615-102">SYNOPSIS</span></span>
<span data-ttu-id="49615-103">Ottiene una connessione trasversale di Azure ExpressRoute da Azure.</span><span class="sxs-lookup"><span data-stu-id="49615-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="49615-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49615-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49615-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49615-105">DESCRIPTION</span></span>
<span data-ttu-id="49615-106">Il cmdlet **Get-AzExpressRouteCrossConnection** viene usato per recuperare un oggetto ExpressRoute Cross Connection dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="49615-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="49615-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="49615-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="49615-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49615-108">EXAMPLES</span></span>

### <span data-ttu-id="49615-109">Esempio 1: ottenere la connessione ExpressRoute Cross</span><span class="sxs-lookup"><span data-stu-id="49615-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="49615-110">Esempio 2: elencare le connessioni incrociate ExpressRoute con un filtro</span><span class="sxs-lookup"><span data-stu-id="49615-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="49615-111">Questo cmdlet elenca tutte le connessioni incrociate ExpressRoute che iniziano con "test"</span><span class="sxs-lookup"><span data-stu-id="49615-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="49615-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49615-112">PARAMETERS</span></span>

### <span data-ttu-id="49615-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49615-113">-DefaultProfile</span></span>
<span data-ttu-id="49615-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49615-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49615-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="49615-115">-Name</span></span>
<span data-ttu-id="49615-116">Il nome della connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="49615-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="49615-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49615-117">-ResourceGroupName</span></span>
<span data-ttu-id="49615-118">Nome del gruppo di risorse che contiene la connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="49615-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="49615-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49615-119">CommonParameters</span></span>
<span data-ttu-id="49615-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49615-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49615-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49615-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49615-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49615-122">INPUTS</span></span>

### <span data-ttu-id="49615-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="49615-123">None</span></span>
<span data-ttu-id="49615-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="49615-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49615-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49615-125">OUTPUTS</span></span>

### <span data-ttu-id="49615-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="49615-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="49615-127">Note</span><span class="sxs-lookup"><span data-stu-id="49615-127">NOTES</span></span>

## <span data-ttu-id="49615-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49615-128">RELATED LINKS</span></span>

[<span data-ttu-id="49615-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="49615-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)