---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 5c341677f5bc741f5848508f80b1a29e29c90b17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954205"
---
# <span data-ttu-id="88255-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="88255-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="88255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88255-102">SYNOPSIS</span></span>
<span data-ttu-id="88255-103">Ottiene una risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="88255-103">Gets a private link resource.</span></span>

## <span data-ttu-id="88255-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88255-104">SYNTAX</span></span>

### <span data-ttu-id="88255-105">ByPrivateLinkResourceId (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88255-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88255-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="88255-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="88255-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="88255-107">DESCRIPTION</span></span>
<span data-ttu-id="88255-108">Il cmdlet **Get-AzPrivateLinkResource** recupera tutte le risorse di collegamento che appartengono a PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="88255-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="88255-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88255-109">EXAMPLES</span></span>

### <span data-ttu-id="88255-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88255-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="88255-111">In questo esempio vengono elencate tutte le risorse di collegamento privato da sql server denominato mySql a sql server.</span><span class="sxs-lookup"><span data-stu-id="88255-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="88255-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88255-112">PARAMETERS</span></span>

### <span data-ttu-id="88255-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88255-113">-DefaultProfile</span></span>
<span data-ttu-id="88255-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88255-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88255-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="88255-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="88255-116">ID manager delle risorse di Azure della risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="88255-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="88255-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="88255-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="88255-118">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="88255-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88255-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88255-119">-ResourceGroupName</span></span>
<span data-ttu-id="88255-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="88255-120">The resource group name.</span></span>

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

### <span data-ttu-id="88255-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="88255-121">-ServiceName</span></span>
<span data-ttu-id="88255-122">Nome del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="88255-122">The private link service name.</span></span>

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

### <span data-ttu-id="88255-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88255-123">CommonParameters</span></span>
<span data-ttu-id="88255-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88255-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88255-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88255-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88255-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="88255-126">INPUTS</span></span>

### <span data-ttu-id="88255-127">System.String</span><span class="sxs-lookup"><span data-stu-id="88255-127">System.String</span></span>

## <span data-ttu-id="88255-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88255-128">OUTPUTS</span></span>

### <span data-ttu-id="88255-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88255-129">System.Boolean</span></span>

## <span data-ttu-id="88255-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="88255-130">NOTES</span></span>

## <span data-ttu-id="88255-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88255-131">RELATED LINKS</span></span>
