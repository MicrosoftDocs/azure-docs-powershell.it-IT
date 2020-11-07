---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7504da022a5cf1310a375bed40370d71d60f205a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853149"
---
# <span data-ttu-id="11fb6-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11fb6-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="11fb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="11fb6-103">Ottiene una risorsa di connessione dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="11fb6-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="11fb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11fb6-104">SYNTAX</span></span>

### <span data-ttu-id="11fb6-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11fb6-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11fb6-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="11fb6-106">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11fb6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11fb6-107">DESCRIPTION</span></span>
<span data-ttu-id="11fb6-108">Il cmdlet **Get-AzPrivateEndpointConnection** recupera una risorsa di connessione endpoint privata.</span><span class="sxs-lookup"><span data-stu-id="11fb6-108">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="11fb6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11fb6-109">EXAMPLES</span></span>

### <span data-ttu-id="11fb6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="11fb6-110">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="11fb6-111">In questo esempio viene ottenuto un collegamento endpoint privato denominato MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="11fb6-111">This example get a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="11fb6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11fb6-112">PARAMETERS</span></span>

### <span data-ttu-id="11fb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11fb6-113">-DefaultProfile</span></span>
<span data-ttu-id="11fb6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11fb6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11fb6-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="11fb6-115">-Description</span></span>
<span data-ttu-id="11fb6-116">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="11fb6-116">The reason of action.</span></span>

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

### <span data-ttu-id="11fb6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="11fb6-117">-Name</span></span>
<span data-ttu-id="11fb6-118">Nome della connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="11fb6-118">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="11fb6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11fb6-119">-ResourceGroupName</span></span>
<span data-ttu-id="11fb6-120">Il nome del gruppo di risorse della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="11fb6-120">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="11fb6-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11fb6-121">-ResourceId</span></span>
<span data-ttu-id="11fb6-122">ID di gestione risorse di Azure della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="11fb6-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="11fb6-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="11fb6-123">-ServiceName</span></span>
<span data-ttu-id="11fb6-124">Nome del servizio di collegamento privato con la connessione dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="11fb6-124">The name of the private link service that has the private endpoint connection.</span></span>

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

### <span data-ttu-id="11fb6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11fb6-125">CommonParameters</span></span>
<span data-ttu-id="11fb6-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11fb6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11fb6-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11fb6-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11fb6-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11fb6-128">INPUTS</span></span>

### <span data-ttu-id="11fb6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="11fb6-129">System.String</span></span>

## <span data-ttu-id="11fb6-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11fb6-130">OUTPUTS</span></span>

### <span data-ttu-id="11fb6-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11fb6-131">System.Boolean</span></span>

## <span data-ttu-id="11fb6-132">Note</span><span class="sxs-lookup"><span data-stu-id="11fb6-132">NOTES</span></span>

## <span data-ttu-id="11fb6-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11fb6-133">RELATED LINKS</span></span>

[<span data-ttu-id="11fb6-134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11fb6-134">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
