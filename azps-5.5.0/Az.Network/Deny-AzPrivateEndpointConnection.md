---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189943"
---
# <span data-ttu-id="7c658-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c658-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="7c658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c658-102">SYNOPSIS</span></span>
<span data-ttu-id="7c658-103">impedisce una connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="7c658-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="7c658-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c658-104">SYNTAX</span></span>

### <span data-ttu-id="7c658-105">ByResourceId (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c658-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c658-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="7c658-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c658-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7c658-107">DESCRIPTION</span></span>
<span data-ttu-id="7c658-108">Il cmdlet **Deny-AzPrivateEndpointConnection** impedisce una connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="7c658-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="7c658-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c658-109">EXAMPLES</span></span>

### <span data-ttu-id="7c658-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c658-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="7c658-111">Questo esempio impedisce una connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="7c658-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="7c658-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c658-112">PARAMETERS</span></span>

### <span data-ttu-id="7c658-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c658-113">-DefaultProfile</span></span>
<span data-ttu-id="7c658-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c658-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c658-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c658-115">-Description</span></span>
<span data-ttu-id="7c658-116">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="7c658-116">The reason of action.</span></span>

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

### <span data-ttu-id="7c658-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7c658-117">-Name</span></span>
<span data-ttu-id="7c658-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c658-118">The resource name.</span></span>

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

### <span data-ttu-id="7c658-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="7c658-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="7c658-120">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="7c658-120">The private link resource type.</span></span>

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

### <span data-ttu-id="7c658-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c658-121">-ResourceGroupName</span></span>
<span data-ttu-id="7c658-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c658-122">The resource group name.</span></span>

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

### <span data-ttu-id="7c658-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c658-123">-ResourceId</span></span>
<span data-ttu-id="7c658-124">ID manager delle risorse di Azure della connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="7c658-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="7c658-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c658-125">-ServiceName</span></span>
<span data-ttu-id="7c658-126">Nome del servizio a cui appartiene la connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="7c658-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="7c658-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c658-127">CommonParameters</span></span>
<span data-ttu-id="7c658-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c658-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c658-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7c658-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c658-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="7c658-130">INPUTS</span></span>

### <span data-ttu-id="7c658-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7c658-131">System.String</span></span>

## <span data-ttu-id="7c658-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c658-132">OUTPUTS</span></span>

### <span data-ttu-id="7c658-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7c658-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="7c658-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="7c658-134">NOTES</span></span>

## <span data-ttu-id="7c658-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c658-135">RELATED LINKS</span></span>

[<span data-ttu-id="7c658-136">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c658-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7c658-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c658-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7c658-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c658-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7c658-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c658-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)