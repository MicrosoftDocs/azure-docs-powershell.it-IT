---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302022"
---
# <span data-ttu-id="657fc-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="657fc-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="657fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="657fc-102">SYNOPSIS</span></span>
<span data-ttu-id="657fc-103">Ottiene una risorsa di connessione dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="657fc-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="657fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="657fc-104">SYNTAX</span></span>

### <span data-ttu-id="657fc-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="657fc-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="657fc-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="657fc-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="657fc-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="657fc-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="657fc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="657fc-108">DESCRIPTION</span></span>
<span data-ttu-id="657fc-109">Il cmdlet **Get-AzPrivateEndpointConnection** recupera una risorsa di connessione endpoint privata.</span><span class="sxs-lookup"><span data-stu-id="657fc-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="657fc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="657fc-110">EXAMPLES</span></span>

### <span data-ttu-id="657fc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="657fc-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="657fc-112">Questo esempio restituisce un elenco di tutte le connessioni di endpoint private appartiene a SQL Server denominato MySQL.</span><span class="sxs-lookup"><span data-stu-id="657fc-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="657fc-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="657fc-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="657fc-114">Questo esempio consente di ottenere una connessione di endpoint privato denominata MyPrivateEndpointConnection1 appartiene al servizio di collegamento privato denominato MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="657fc-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="657fc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="657fc-115">PARAMETERS</span></span>

### <span data-ttu-id="657fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="657fc-116">-DefaultProfile</span></span>
<span data-ttu-id="657fc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="657fc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="657fc-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="657fc-118">-Description</span></span>
<span data-ttu-id="657fc-119">Il motivo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="657fc-119">The reason of action.</span></span>

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

### <span data-ttu-id="657fc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="657fc-120">-Name</span></span>
<span data-ttu-id="657fc-121">Nome della connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="657fc-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="657fc-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="657fc-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="657fc-123">ID di gestione risorse di Azure della risorsa di collegamento privato a cui appartiene la connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="657fc-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="657fc-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="657fc-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="657fc-125">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="657fc-125">The private link resource type.</span></span>

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

### <span data-ttu-id="657fc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="657fc-126">-ResourceGroupName</span></span>
<span data-ttu-id="657fc-127">Il nome del gruppo di risorse della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="657fc-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="657fc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="657fc-128">-ResourceId</span></span>
<span data-ttu-id="657fc-129">ID di gestione risorse di Azure della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="657fc-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="657fc-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="657fc-130">-ServiceName</span></span>
<span data-ttu-id="657fc-131">Nome del servizio a cui appartiene la connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="657fc-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="657fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="657fc-132">CommonParameters</span></span>
<span data-ttu-id="657fc-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="657fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="657fc-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="657fc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="657fc-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="657fc-135">INPUTS</span></span>

### <span data-ttu-id="657fc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="657fc-136">System.String</span></span>

## <span data-ttu-id="657fc-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="657fc-137">OUTPUTS</span></span>

### <span data-ttu-id="657fc-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="657fc-138">System.Boolean</span></span>

## <span data-ttu-id="657fc-139">Note</span><span class="sxs-lookup"><span data-stu-id="657fc-139">NOTES</span></span>

## <span data-ttu-id="657fc-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="657fc-140">RELATED LINKS</span></span>

[<span data-ttu-id="657fc-141">Approva-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="657fc-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="657fc-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="657fc-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="657fc-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="657fc-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="657fc-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="657fc-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
