---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 4a67914fd3709ef972adac8eba6b1b2fa211fbf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853342"
---
# <span data-ttu-id="849c7-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="849c7-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="849c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="849c7-102">SYNOPSIS</span></span>
<span data-ttu-id="849c7-103">nega una connessione a un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="849c7-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="849c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="849c7-104">SYNTAX</span></span>

### <span data-ttu-id="849c7-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="849c7-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="849c7-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="849c7-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="849c7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="849c7-107">DESCRIPTION</span></span>
<span data-ttu-id="849c7-108">Il cmdlet **Deny-AzPrivateEndpointConnection** nega una connessione a un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="849c7-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="849c7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="849c7-109">EXAMPLES</span></span>

### <span data-ttu-id="849c7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="849c7-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="849c7-111">Questo esempio nega una connessione a un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="849c7-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="849c7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="849c7-112">PARAMETERS</span></span>

### <span data-ttu-id="849c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849c7-113">-DefaultProfile</span></span>
<span data-ttu-id="849c7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="849c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="849c7-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="849c7-115">-Description</span></span>
<span data-ttu-id="849c7-116">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="849c7-116">The reason of action.</span></span>

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

### <span data-ttu-id="849c7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="849c7-117">-Name</span></span>
<span data-ttu-id="849c7-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="849c7-118">The resource name.</span></span>

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

### <span data-ttu-id="849c7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="849c7-119">-ResourceGroupName</span></span>
<span data-ttu-id="849c7-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="849c7-120">The resource group name.</span></span>

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

### <span data-ttu-id="849c7-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="849c7-121">-ResourceId</span></span>
<span data-ttu-id="849c7-122">ID di gestione risorse di Azure della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="849c7-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="849c7-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="849c7-123">-ServiceName</span></span>
<span data-ttu-id="849c7-124">Nome del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="849c7-124">The private link service name.</span></span>

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

### <span data-ttu-id="849c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849c7-125">CommonParameters</span></span>
<span data-ttu-id="849c7-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849c7-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="849c7-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849c7-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="849c7-128">INPUTS</span></span>

### <span data-ttu-id="849c7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="849c7-129">System.String</span></span>

## <span data-ttu-id="849c7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="849c7-130">OUTPUTS</span></span>

### <span data-ttu-id="849c7-131">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="849c7-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="849c7-132">Note</span><span class="sxs-lookup"><span data-stu-id="849c7-132">NOTES</span></span>

## <span data-ttu-id="849c7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="849c7-133">RELATED LINKS</span></span>

[<span data-ttu-id="849c7-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="849c7-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="849c7-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="849c7-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="849c7-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="849c7-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)