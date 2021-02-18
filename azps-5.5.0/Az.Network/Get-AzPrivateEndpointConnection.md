---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184727"
---
# <span data-ttu-id="f6d94-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f6d94-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="f6d94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6d94-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d94-103">Ottiene una risorsa di connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="f6d94-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="f6d94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6d94-104">SYNTAX</span></span>

### <span data-ttu-id="f6d94-105">ByResourceId (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6d94-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6d94-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f6d94-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6d94-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="f6d94-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6d94-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f6d94-108">DESCRIPTION</span></span>
<span data-ttu-id="f6d94-109">Il cmdlet **Get-AzPrivateEndpointConnection** recupera una risorsa di connessione all'endpoint privata.</span><span class="sxs-lookup"><span data-stu-id="f6d94-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="f6d94-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6d94-110">EXAMPLES</span></span>

### <span data-ttu-id="f6d94-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f6d94-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="f6d94-112">Questo esempio restituisce un elenco di tutte le connessioni endpoint private appartenenti a un server sql denominato Mysql.</span><span class="sxs-lookup"><span data-stu-id="f6d94-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="f6d94-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f6d94-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="f6d94-114">Questo esempio ottiene una connessione all'endpoint privato denominata MyPrivateEndpointConnection1 appartiene al servizio di collegamento privato denominato MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f6d94-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="f6d94-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6d94-115">PARAMETERS</span></span>

### <span data-ttu-id="f6d94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d94-116">-DefaultProfile</span></span>
<span data-ttu-id="f6d94-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6d94-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6d94-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6d94-118">-Description</span></span>
<span data-ttu-id="f6d94-119">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="f6d94-119">The reason of action.</span></span>

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

### <span data-ttu-id="f6d94-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f6d94-120">-Name</span></span>
<span data-ttu-id="f6d94-121">Nome della connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="f6d94-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="f6d94-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f6d94-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="f6d94-123">ID manager delle risorse di Azure della risorsa collegamento privato a cui appartiene la connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="f6d94-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="f6d94-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="f6d94-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="f6d94-125">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="f6d94-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values: 

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6d94-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6d94-126">-ResourceGroupName</span></span>
<span data-ttu-id="f6d94-127">Nome del gruppo di risorse della connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="f6d94-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="f6d94-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6d94-128">-ResourceId</span></span>
<span data-ttu-id="f6d94-129">ID manager delle risorse di Azure della connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="f6d94-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="f6d94-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f6d94-130">-ServiceName</span></span>
<span data-ttu-id="f6d94-131">Nome del servizio a cui appartiene la connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="f6d94-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="f6d94-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d94-132">CommonParameters</span></span>
<span data-ttu-id="f6d94-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6d94-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d94-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f6d94-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d94-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="f6d94-135">INPUTS</span></span>

### <span data-ttu-id="f6d94-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f6d94-136">System.String</span></span>

## <span data-ttu-id="f6d94-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6d94-137">OUTPUTS</span></span>

### <span data-ttu-id="f6d94-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6d94-138">System.Boolean</span></span>

## <span data-ttu-id="f6d94-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="f6d94-139">NOTES</span></span>

## <span data-ttu-id="f6d94-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6d94-140">RELATED LINKS</span></span>

[<span data-ttu-id="f6d94-141">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f6d94-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f6d94-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f6d94-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f6d94-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f6d94-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f6d94-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f6d94-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
