---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202844"
---
# <span data-ttu-id="7f18c-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7f18c-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7f18c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f18c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f18c-103">Ottiene una connessione trasversale di Azure ExpressRoute da Azure.</span><span class="sxs-lookup"><span data-stu-id="7f18c-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="7f18c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f18c-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f18c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f18c-105">DESCRIPTION</span></span>
<span data-ttu-id="7f18c-106">Il cmdlet **Get-AzExpressRouteCrossConnection** viene usato per recuperare un oggetto ExpressRoute Cross Connection dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7f18c-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="7f18c-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7f18c-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7f18c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f18c-108">EXAMPLES</span></span>

### <span data-ttu-id="7f18c-109">Esempio 1: ottenere la connessione ExpressRoute Cross</span><span class="sxs-lookup"><span data-stu-id="7f18c-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="7f18c-110">Esempio 2: elencare le connessioni incrociate ExpressRoute con un filtro</span><span class="sxs-lookup"><span data-stu-id="7f18c-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="7f18c-111">Questo cmdlet elenca tutte le connessioni incrociate ExpressRoute che iniziano con "test"</span><span class="sxs-lookup"><span data-stu-id="7f18c-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="7f18c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f18c-112">PARAMETERS</span></span>

### <span data-ttu-id="7f18c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f18c-113">-DefaultProfile</span></span>
<span data-ttu-id="7f18c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f18c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f18c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f18c-115">-Name</span></span>
<span data-ttu-id="7f18c-116">Il nome della connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7f18c-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="7f18c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f18c-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f18c-118">Nome del gruppo di risorse che contiene la connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7f18c-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="7f18c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f18c-119">CommonParameters</span></span>
<span data-ttu-id="7f18c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f18c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f18c-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f18c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f18c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f18c-122">INPUTS</span></span>

### <span data-ttu-id="7f18c-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7f18c-123">None</span></span>
<span data-ttu-id="7f18c-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7f18c-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f18c-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f18c-125">OUTPUTS</span></span>

### <span data-ttu-id="7f18c-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7f18c-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7f18c-127">Note</span><span class="sxs-lookup"><span data-stu-id="7f18c-127">NOTES</span></span>

## <span data-ttu-id="7f18c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f18c-128">RELATED LINKS</span></span>

[<span data-ttu-id="7f18c-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7f18c-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)