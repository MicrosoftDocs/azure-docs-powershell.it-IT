---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 3768bc8769d81056dc8f2de4f42f9f1783f89728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979645"
---
# <span data-ttu-id="82c78-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="82c78-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="82c78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82c78-102">SYNOPSIS</span></span>
<span data-ttu-id="82c78-103">Approva una connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="82c78-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="82c78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82c78-104">SYNTAX</span></span>

### <span data-ttu-id="82c78-105">ByResourceId (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82c78-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82c78-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="82c78-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c78-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="82c78-107">DESCRIPTION</span></span>
<span data-ttu-id="82c78-108">Il cmdlet **Approve-AzPrivateEndpointConnection** approva una connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="82c78-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="82c78-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82c78-109">EXAMPLES</span></span>

### <span data-ttu-id="82c78-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82c78-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="82c78-111">Questo esempio approva una connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="82c78-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="82c78-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82c78-112">PARAMETERS</span></span>

### <span data-ttu-id="82c78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c78-113">-DefaultProfile</span></span>
<span data-ttu-id="82c78-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82c78-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82c78-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="82c78-115">-Description</span></span>
<span data-ttu-id="82c78-116">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="82c78-116">The reason of action.</span></span>

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

### <span data-ttu-id="82c78-117">-Name</span><span class="sxs-lookup"><span data-stu-id="82c78-117">-Name</span></span>
<span data-ttu-id="82c78-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="82c78-118">The resource name.</span></span>

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

### <span data-ttu-id="82c78-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="82c78-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="82c78-120">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="82c78-120">The private link resource type.</span></span>

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

### <span data-ttu-id="82c78-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c78-121">-ResourceGroupName</span></span>
<span data-ttu-id="82c78-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="82c78-122">The resource group name.</span></span>

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

### <span data-ttu-id="82c78-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82c78-123">-ResourceId</span></span>
<span data-ttu-id="82c78-124">ID manager delle risorse di Azure della connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="82c78-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="82c78-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="82c78-125">-ServiceName</span></span>
<span data-ttu-id="82c78-126">Nome del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="82c78-126">The private link service name.</span></span>

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


### <span data-ttu-id="82c78-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c78-127">CommonParameters</span></span>
<span data-ttu-id="82c78-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c78-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c78-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82c78-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c78-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="82c78-130">INPUTS</span></span>

### <span data-ttu-id="82c78-131">System.String</span><span class="sxs-lookup"><span data-stu-id="82c78-131">System.String</span></span>

## <span data-ttu-id="82c78-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82c78-132">OUTPUTS</span></span>

### <span data-ttu-id="82c78-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="82c78-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="82c78-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="82c78-134">NOTES</span></span>

## <span data-ttu-id="82c78-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82c78-135">RELATED LINKS</span></span>

[<span data-ttu-id="82c78-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="82c78-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="82c78-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="82c78-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="82c78-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="82c78-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="82c78-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="82c78-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)