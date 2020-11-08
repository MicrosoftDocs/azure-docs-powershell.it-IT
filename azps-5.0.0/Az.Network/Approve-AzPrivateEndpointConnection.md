---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202310"
---
# <span data-ttu-id="aaf65-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="aaf65-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="aaf65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aaf65-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf65-103">Approva una connessione di endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="aaf65-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="aaf65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaf65-104">SYNTAX</span></span>

### <span data-ttu-id="aaf65-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aaf65-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaf65-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="aaf65-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaf65-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaf65-107">DESCRIPTION</span></span>
<span data-ttu-id="aaf65-108">Il cmdlet **Approval-AzPrivateEndpointConnection** approva una connessione a un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="aaf65-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="aaf65-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaf65-109">EXAMPLES</span></span>

### <span data-ttu-id="aaf65-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aaf65-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="aaf65-111">Questo esempio approva una connessione di endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="aaf65-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="aaf65-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aaf65-112">PARAMETERS</span></span>

### <span data-ttu-id="aaf65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf65-113">-DefaultProfile</span></span>
<span data-ttu-id="aaf65-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf65-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaf65-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaf65-115">-Description</span></span>
<span data-ttu-id="aaf65-116">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="aaf65-116">The reason of action.</span></span>

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

### <span data-ttu-id="aaf65-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="aaf65-117">-Name</span></span>
<span data-ttu-id="aaf65-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="aaf65-118">The resource name.</span></span>

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

### <span data-ttu-id="aaf65-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="aaf65-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="aaf65-120">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="aaf65-120">The private link resource type.</span></span>

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

### <span data-ttu-id="aaf65-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf65-121">-ResourceGroupName</span></span>
<span data-ttu-id="aaf65-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aaf65-122">The resource group name.</span></span>

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

### <span data-ttu-id="aaf65-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaf65-123">-ResourceId</span></span>
<span data-ttu-id="aaf65-124">ID di gestione risorse di Azure della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="aaf65-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="aaf65-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aaf65-125">-ServiceName</span></span>
<span data-ttu-id="aaf65-126">Nome del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="aaf65-126">The private link service name.</span></span>

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


### <span data-ttu-id="aaf65-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf65-127">CommonParameters</span></span>
<span data-ttu-id="aaf65-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf65-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf65-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aaf65-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf65-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aaf65-130">INPUTS</span></span>

### <span data-ttu-id="aaf65-131">System. String</span><span class="sxs-lookup"><span data-stu-id="aaf65-131">System.String</span></span>

## <span data-ttu-id="aaf65-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaf65-132">OUTPUTS</span></span>

### <span data-ttu-id="aaf65-133">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="aaf65-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="aaf65-134">Note</span><span class="sxs-lookup"><span data-stu-id="aaf65-134">NOTES</span></span>

## <span data-ttu-id="aaf65-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaf65-135">RELATED LINKS</span></span>

[<span data-ttu-id="aaf65-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="aaf65-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="aaf65-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="aaf65-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="aaf65-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="aaf65-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="aaf65-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="aaf65-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)