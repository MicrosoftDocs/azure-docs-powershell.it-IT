---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381023"
---
# <span data-ttu-id="7cd58-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7cd58-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="7cd58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cd58-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd58-103">Ottiene una risorsa di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="7cd58-103">Gets a private link resource.</span></span>

## <span data-ttu-id="7cd58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cd58-104">SYNTAX</span></span>

### <span data-ttu-id="7cd58-105">ByPrivateLinkResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7cd58-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7cd58-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="7cd58-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="7cd58-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cd58-107">DESCRIPTION</span></span>
<span data-ttu-id="7cd58-108">Il cmdlet **Get-AzPrivateLinkResource** recupera tutte le risorse di collegamento appartiene PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="7cd58-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="7cd58-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cd58-109">EXAMPLES</span></span>

### <span data-ttu-id="7cd58-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7cd58-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="7cd58-111">Questo esempio elenca tutte le risorse del collegamento privato nbelong a SQL Server denominato mySql.</span><span class="sxs-lookup"><span data-stu-id="7cd58-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="7cd58-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cd58-112">PARAMETERS</span></span>

### <span data-ttu-id="7cd58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd58-113">-DefaultProfile</span></span>
<span data-ttu-id="7cd58-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cd58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cd58-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd58-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="7cd58-116">ID di gestione risorse di Azure della risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="7cd58-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="7cd58-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="7cd58-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="7cd58-118">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="7cd58-118">The private link resource type.</span></span>

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

### <span data-ttu-id="7cd58-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd58-119">-ResourceGroupName</span></span>
<span data-ttu-id="7cd58-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7cd58-120">The resource group name.</span></span>

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

### <span data-ttu-id="7cd58-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7cd58-121">-ServiceName</span></span>
<span data-ttu-id="7cd58-122">Nome del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="7cd58-122">The private link service name.</span></span>

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

### <span data-ttu-id="7cd58-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd58-123">CommonParameters</span></span>
<span data-ttu-id="7cd58-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd58-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd58-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cd58-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd58-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cd58-126">INPUTS</span></span>

### <span data-ttu-id="7cd58-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7cd58-127">System.String</span></span>

## <span data-ttu-id="7cd58-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cd58-128">OUTPUTS</span></span>

### <span data-ttu-id="7cd58-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7cd58-129">System.Boolean</span></span>

## <span data-ttu-id="7cd58-130">Note</span><span class="sxs-lookup"><span data-stu-id="7cd58-130">NOTES</span></span>

## <span data-ttu-id="7cd58-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cd58-131">RELATED LINKS</span></span>
