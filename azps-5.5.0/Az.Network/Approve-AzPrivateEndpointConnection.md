---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206995"
---
# <span data-ttu-id="6ddb9-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ddb9-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="6ddb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ddb9-102">SYNOPSIS</span></span>
<span data-ttu-id="6ddb9-103">Approva una connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="6ddb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ddb9-104">SYNTAX</span></span>

### <span data-ttu-id="6ddb9-105">ByResourceId (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ddb9-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ddb9-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="6ddb9-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ddb9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6ddb9-107">DESCRIPTION</span></span>
<span data-ttu-id="6ddb9-108">Il cmdlet **Approve-AzPrivateEndpointConnection** approva una connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="6ddb9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ddb9-109">EXAMPLES</span></span>

### <span data-ttu-id="6ddb9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ddb9-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="6ddb9-111">Questo esempio approva una connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="6ddb9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ddb9-112">PARAMETERS</span></span>

### <span data-ttu-id="6ddb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ddb9-113">-DefaultProfile</span></span>
<span data-ttu-id="6ddb9-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ddb9-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ddb9-115">-Description</span></span>
<span data-ttu-id="6ddb9-116">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-116">The reason of action.</span></span>

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

### <span data-ttu-id="6ddb9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6ddb9-117">-Name</span></span>
<span data-ttu-id="6ddb9-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-118">The resource name.</span></span>

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

### <span data-ttu-id="6ddb9-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="6ddb9-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="6ddb9-120">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-120">The private link resource type.</span></span>

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

### <span data-ttu-id="6ddb9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ddb9-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ddb9-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-122">The resource group name.</span></span>

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

### <span data-ttu-id="6ddb9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ddb9-123">-ResourceId</span></span>
<span data-ttu-id="6ddb9-124">ID manager delle risorse di Azure della connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="6ddb9-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6ddb9-125">-ServiceName</span></span>
<span data-ttu-id="6ddb9-126">Nome del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-126">The private link service name.</span></span>

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


### <span data-ttu-id="6ddb9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ddb9-127">CommonParameters</span></span>
<span data-ttu-id="6ddb9-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ddb9-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6ddb9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ddb9-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="6ddb9-130">INPUTS</span></span>

### <span data-ttu-id="6ddb9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6ddb9-131">System.String</span></span>

## <span data-ttu-id="6ddb9-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ddb9-132">OUTPUTS</span></span>

### <span data-ttu-id="6ddb9-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6ddb9-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="6ddb9-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="6ddb9-134">NOTES</span></span>

## <span data-ttu-id="6ddb9-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ddb9-135">RELATED LINKS</span></span>

[<span data-ttu-id="6ddb9-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ddb9-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="6ddb9-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ddb9-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="6ddb9-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ddb9-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="6ddb9-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ddb9-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)