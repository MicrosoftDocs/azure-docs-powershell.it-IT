---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193358"
---
# <span data-ttu-id="f9e29-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e29-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="f9e29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9e29-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e29-103">Aggiorna lo stato di connessione di un endpoint privato nel servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="f9e29-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="f9e29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9e29-104">SYNTAX</span></span>

### <span data-ttu-id="f9e29-105">ByResourceId (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9e29-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9e29-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="f9e29-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9e29-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f9e29-107">DESCRIPTION</span></span>
<span data-ttu-id="f9e29-108">Il cmdlet **Set-AzPrivateEndpointConnection** aggiorna lo stato di connessione di un endpoint privato in un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="f9e29-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="f9e29-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9e29-109">EXAMPLES</span></span>

### <span data-ttu-id="f9e29-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f9e29-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="f9e29-111">Questo esempio aggiorna lo stato di connessione di un endpoint privato ad Approvato.</span><span class="sxs-lookup"><span data-stu-id="f9e29-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="f9e29-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9e29-112">PARAMETERS</span></span>

### <span data-ttu-id="f9e29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e29-113">-DefaultProfile</span></span>
<span data-ttu-id="f9e29-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e29-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9e29-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9e29-115">-Description</span></span>
<span data-ttu-id="f9e29-116">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="f9e29-116">The reason of action.</span></span>

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

### <span data-ttu-id="f9e29-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f9e29-117">-Name</span></span>
<span data-ttu-id="f9e29-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f9e29-118">The resource name.</span></span>

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

### <span data-ttu-id="f9e29-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="f9e29-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="f9e29-120">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="f9e29-120">The private link resource type.</span></span>

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

### <span data-ttu-id="f9e29-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="f9e29-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="f9e29-122">Approvata o rifiutata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f9e29-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="f9e29-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e29-123">-ResourceGroupName</span></span>
<span data-ttu-id="f9e29-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9e29-124">The resource group name.</span></span>

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

### <span data-ttu-id="f9e29-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e29-125">-ResourceId</span></span>
<span data-ttu-id="f9e29-126">ID manager delle risorse di Azure della connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="f9e29-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="f9e29-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f9e29-127">-ServiceName</span></span>
<span data-ttu-id="f9e29-128">Nome del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="f9e29-128">The private link service name.</span></span>

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

### <span data-ttu-id="f9e29-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e29-129">CommonParameters</span></span>
<span data-ttu-id="f9e29-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9e29-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e29-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9e29-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e29-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="f9e29-132">INPUTS</span></span>

### <span data-ttu-id="f9e29-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f9e29-133">System.String</span></span>

## <span data-ttu-id="f9e29-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9e29-134">OUTPUTS</span></span>

### <span data-ttu-id="f9e29-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9e29-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="f9e29-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="f9e29-136">NOTES</span></span>

## <span data-ttu-id="f9e29-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9e29-137">RELATED LINKS</span></span>

[<span data-ttu-id="f9e29-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e29-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f9e29-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e29-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f9e29-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e29-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f9e29-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9e29-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)