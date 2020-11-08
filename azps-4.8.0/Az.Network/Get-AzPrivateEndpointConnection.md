---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 30b156a7adc972d06e514dd3d8d27c40f41194df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189010"
---
# <span data-ttu-id="0c334-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c334-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="0c334-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c334-102">SYNOPSIS</span></span>
<span data-ttu-id="0c334-103">Ottiene una risorsa di connessione dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="0c334-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="0c334-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c334-104">SYNTAX</span></span>

### <span data-ttu-id="0c334-105">ByPrivateLinkResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c334-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c334-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c334-106">ByResourceId</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c334-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="0c334-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -ServiceName <String> -ResourceGroupName <String>
[-Name <String>] [-PrivateLinkResourceType <String>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c334-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c334-108">DESCRIPTION</span></span>
<span data-ttu-id="0c334-109">Il cmdlet **Get-AzPrivateEndpointConnection** recupera una risorsa di connessione endpoint privata.</span><span class="sxs-lookup"><span data-stu-id="0c334-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="0c334-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c334-110">EXAMPLES</span></span>

### <span data-ttu-id="0c334-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c334-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="0c334-112">Questo esempio restituisce un elenco di tutte le connessioni di endpoint private appartiene a SQL Server denominato MySQL.</span><span class="sxs-lookup"><span data-stu-id="0c334-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="0c334-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0c334-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="0c334-114">Questo esempio consente di ottenere una connessione di endpoint privato denominata MyPrivateEndpointConnection1 appartiene al servizio di collegamento privato denominato MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0c334-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="0c334-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c334-115">PARAMETERS</span></span>

### <span data-ttu-id="0c334-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c334-116">-DefaultProfile</span></span>
<span data-ttu-id="0c334-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c334-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c334-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c334-118">-Name</span></span>
<span data-ttu-id="0c334-119">Nome della connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="0c334-119">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c334-120">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="0c334-120">-PrivateLinkResourceId</span></span>
<span data-ttu-id="0c334-121">ID di gestione risorse di Azure della risorsa di collegamento privato a cui appartiene la connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="0c334-121">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c334-122">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="0c334-122">-PrivateLinkResourceType</span></span>
<span data-ttu-id="0c334-123">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="0c334-123">The private link resource type.</span></span>

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

### <span data-ttu-id="0c334-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c334-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c334-125">Il nome del gruppo di risorse della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="0c334-125">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="0c334-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c334-126">-ResourceId</span></span>
<span data-ttu-id="0c334-127">ID di gestione risorse di Azure della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="0c334-127">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="0c334-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0c334-128">-ServiceName</span></span>
<span data-ttu-id="0c334-129">Nome del servizio a cui appartiene la connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="0c334-129">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="0c334-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c334-130">CommonParameters</span></span>
<span data-ttu-id="0c334-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c334-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c334-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c334-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c334-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c334-133">INPUTS</span></span>

### <span data-ttu-id="0c334-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0c334-134">System.String</span></span>

## <span data-ttu-id="0c334-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c334-135">OUTPUTS</span></span>

### <span data-ttu-id="0c334-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c334-136">System.Boolean</span></span>

## <span data-ttu-id="0c334-137">Note</span><span class="sxs-lookup"><span data-stu-id="0c334-137">NOTES</span></span>

## <span data-ttu-id="0c334-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c334-138">RELATED LINKS</span></span>

[<span data-ttu-id="0c334-139">Approva-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c334-139">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c334-140">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c334-140">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c334-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c334-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c334-142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c334-142">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
