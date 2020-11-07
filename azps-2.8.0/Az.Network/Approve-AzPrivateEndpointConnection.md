---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9b47fb1954b13e28268f6b7aad66fa8190e20584
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853350"
---
# <span data-ttu-id="c316d-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c316d-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="c316d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c316d-102">SYNOPSIS</span></span>
<span data-ttu-id="c316d-103">Approva una connessione di endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="c316d-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="c316d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c316d-104">SYNTAX</span></span>

### <span data-ttu-id="c316d-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c316d-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c316d-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="c316d-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c316d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c316d-107">DESCRIPTION</span></span>
<span data-ttu-id="c316d-108">Il cmdlet **Approval-AzPrivateEndpointConnection** approva una connessione a un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="c316d-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="c316d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c316d-109">EXAMPLES</span></span>

### <span data-ttu-id="c316d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c316d-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="c316d-111">Questo esempio approva una connessione di endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="c316d-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="c316d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c316d-112">PARAMETERS</span></span>

### <span data-ttu-id="c316d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c316d-113">-DefaultProfile</span></span>
<span data-ttu-id="c316d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c316d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c316d-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c316d-115">-Description</span></span>
<span data-ttu-id="c316d-116">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="c316d-116">The reason of action.</span></span>

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

### <span data-ttu-id="c316d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c316d-117">-Name</span></span>
<span data-ttu-id="c316d-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c316d-118">The resource name.</span></span>

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

### <span data-ttu-id="c316d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c316d-119">-ResourceGroupName</span></span>
<span data-ttu-id="c316d-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c316d-120">The resource group name.</span></span>

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

### <span data-ttu-id="c316d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c316d-121">-ResourceId</span></span>
<span data-ttu-id="c316d-122">ID di gestione risorse di Azure della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="c316d-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="c316d-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c316d-123">-ServiceName</span></span>
<span data-ttu-id="c316d-124">Nome del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="c316d-124">The private link service name.</span></span>

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

### <span data-ttu-id="c316d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c316d-125">CommonParameters</span></span>
<span data-ttu-id="c316d-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c316d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c316d-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c316d-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c316d-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c316d-128">INPUTS</span></span>

### <span data-ttu-id="c316d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c316d-129">System.String</span></span>

## <span data-ttu-id="c316d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c316d-130">OUTPUTS</span></span>

### <span data-ttu-id="c316d-131">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c316d-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="c316d-132">Note</span><span class="sxs-lookup"><span data-stu-id="c316d-132">NOTES</span></span>

## <span data-ttu-id="c316d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c316d-133">RELATED LINKS</span></span>

[<span data-ttu-id="c316d-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c316d-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c316d-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c316d-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c316d-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c316d-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)