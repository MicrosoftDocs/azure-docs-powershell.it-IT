---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 588402480cbd626a747208705ec59fd10c572075
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855222"
---
# <span data-ttu-id="2dcb2-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2dcb2-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="2dcb2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2dcb2-102">SYNOPSIS</span></span>
<span data-ttu-id="2dcb2-103">Aggiorna uno stato di connessione endpoint privato sul servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="2dcb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2dcb2-104">SYNTAX</span></span>

```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2dcb2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dcb2-105">DESCRIPTION</span></span>
<span data-ttu-id="2dcb2-106">Il cmdlet **set-AzPrivateEndpointConnection** aggiorna uno stato di connessione endpoint privato in un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="2dcb2-106">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="2dcb2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2dcb2-107">EXAMPLES</span></span>

### <span data-ttu-id="2dcb2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2dcb2-108">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="2dcb2-109">Questo esempio aggiorna uno stato di connessione endpoint privato in approvato.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-109">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="2dcb2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2dcb2-110">PARAMETERS</span></span>

### <span data-ttu-id="2dcb2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dcb2-111">-DefaultProfile</span></span>
<span data-ttu-id="2dcb2-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dcb2-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dcb2-113">-Description</span></span>
<span data-ttu-id="2dcb2-114">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-114">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dcb2-115">-Name</span></span>
<span data-ttu-id="2dcb2-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb2-117">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="2dcb2-117">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="2dcb2-118">Approvato o rifiutato la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-118">Approved or rejected the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dcb2-119">-ResourceGroupName</span></span>
<span data-ttu-id="2dcb2-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb2-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2dcb2-121">-ServiceName</span></span>
<span data-ttu-id="2dcb2-122">Nome del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-122">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dcb2-123">CommonParameters</span></span>
<span data-ttu-id="2dcb2-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dcb2-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dcb2-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dcb2-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2dcb2-126">INPUTS</span></span>

### <span data-ttu-id="2dcb2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2dcb2-127">System.String</span></span>

## <span data-ttu-id="2dcb2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2dcb2-128">OUTPUTS</span></span>

### <span data-ttu-id="2dcb2-129">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2dcb2-129">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="2dcb2-130">Note</span><span class="sxs-lookup"><span data-stu-id="2dcb2-130">NOTES</span></span>

## <span data-ttu-id="2dcb2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2dcb2-131">RELATED LINKS</span></span>
