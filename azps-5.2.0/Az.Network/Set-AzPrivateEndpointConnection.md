---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344176"
---
# <span data-ttu-id="896f6-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="896f6-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="896f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="896f6-102">SYNOPSIS</span></span>
<span data-ttu-id="896f6-103">Aggiorna uno stato di connessione endpoint privato sul servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="896f6-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="896f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="896f6-104">SYNTAX</span></span>

### <span data-ttu-id="896f6-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="896f6-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="896f6-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="896f6-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="896f6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="896f6-107">DESCRIPTION</span></span>
<span data-ttu-id="896f6-108">Il cmdlet **set-AzPrivateEndpointConnection** aggiorna uno stato di connessione endpoint privato in un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="896f6-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="896f6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="896f6-109">EXAMPLES</span></span>

### <span data-ttu-id="896f6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="896f6-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="896f6-111">Questo esempio aggiorna uno stato di connessione endpoint privato in approvato.</span><span class="sxs-lookup"><span data-stu-id="896f6-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="896f6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="896f6-112">PARAMETERS</span></span>

### <span data-ttu-id="896f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="896f6-113">-DefaultProfile</span></span>
<span data-ttu-id="896f6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="896f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="896f6-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="896f6-115">-Description</span></span>
<span data-ttu-id="896f6-116">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="896f6-116">The reason of action.</span></span>

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

### <span data-ttu-id="896f6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="896f6-117">-Name</span></span>
<span data-ttu-id="896f6-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="896f6-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="896f6-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="896f6-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="896f6-120">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="896f6-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="896f6-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="896f6-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="896f6-122">Approvato o rifiutato la risorsa.</span><span class="sxs-lookup"><span data-stu-id="896f6-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="896f6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="896f6-123">-ResourceGroupName</span></span>
<span data-ttu-id="896f6-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="896f6-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="896f6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="896f6-125">-ResourceId</span></span>
<span data-ttu-id="896f6-126">ID di gestione risorse di Azure della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="896f6-126">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="896f6-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="896f6-127">-ServiceName</span></span>
<span data-ttu-id="896f6-128">Nome del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="896f6-128">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="896f6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="896f6-129">CommonParameters</span></span>
<span data-ttu-id="896f6-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="896f6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="896f6-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="896f6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="896f6-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="896f6-132">INPUTS</span></span>

### <span data-ttu-id="896f6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="896f6-133">System.String</span></span>

## <span data-ttu-id="896f6-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="896f6-134">OUTPUTS</span></span>

### <span data-ttu-id="896f6-135">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="896f6-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="896f6-136">Note</span><span class="sxs-lookup"><span data-stu-id="896f6-136">NOTES</span></span>

## <span data-ttu-id="896f6-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="896f6-137">RELATED LINKS</span></span>

[<span data-ttu-id="896f6-138">Approva-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="896f6-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="896f6-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="896f6-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="896f6-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="896f6-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="896f6-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="896f6-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)