---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201840"
---
# <span data-ttu-id="b86cf-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b86cf-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="b86cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b86cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b86cf-103">nega una connessione a un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="b86cf-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="b86cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b86cf-104">SYNTAX</span></span>

### <span data-ttu-id="b86cf-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b86cf-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b86cf-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="b86cf-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b86cf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b86cf-107">DESCRIPTION</span></span>
<span data-ttu-id="b86cf-108">Il cmdlet **Deny-AzPrivateEndpointConnection** nega una connessione a un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="b86cf-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="b86cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b86cf-109">EXAMPLES</span></span>

### <span data-ttu-id="b86cf-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b86cf-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="b86cf-111">Questo esempio nega una connessione a un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="b86cf-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="b86cf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b86cf-112">PARAMETERS</span></span>

### <span data-ttu-id="b86cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b86cf-113">-DefaultProfile</span></span>
<span data-ttu-id="b86cf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b86cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b86cf-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b86cf-115">-Description</span></span>
<span data-ttu-id="b86cf-116">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="b86cf-116">The reason of action.</span></span>

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

### <span data-ttu-id="b86cf-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b86cf-117">-Name</span></span>
<span data-ttu-id="b86cf-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b86cf-118">The resource name.</span></span>

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

### <span data-ttu-id="b86cf-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="b86cf-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="b86cf-120">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="b86cf-120">The private link resource type.</span></span>

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

### <span data-ttu-id="b86cf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b86cf-121">-ResourceGroupName</span></span>
<span data-ttu-id="b86cf-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b86cf-122">The resource group name.</span></span>

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

### <span data-ttu-id="b86cf-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b86cf-123">-ResourceId</span></span>
<span data-ttu-id="b86cf-124">ID di gestione risorse di Azure della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="b86cf-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="b86cf-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b86cf-125">-ServiceName</span></span>
<span data-ttu-id="b86cf-126">Nome del servizio a cui appartiene la connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="b86cf-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="b86cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86cf-127">CommonParameters</span></span>
<span data-ttu-id="b86cf-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b86cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86cf-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b86cf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86cf-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b86cf-130">INPUTS</span></span>

### <span data-ttu-id="b86cf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b86cf-131">System.String</span></span>

## <span data-ttu-id="b86cf-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b86cf-132">OUTPUTS</span></span>

### <span data-ttu-id="b86cf-133">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b86cf-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="b86cf-134">Note</span><span class="sxs-lookup"><span data-stu-id="b86cf-134">NOTES</span></span>

## <span data-ttu-id="b86cf-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b86cf-135">RELATED LINKS</span></span>

[<span data-ttu-id="b86cf-136">Approva-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b86cf-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b86cf-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b86cf-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b86cf-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b86cf-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b86cf-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b86cf-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)