---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 3ba277ccee3a07f71677628fdc0a985225cdf724
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021261"
---
# <span data-ttu-id="a9d7c-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a9d7c-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="a9d7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9d7c-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d7c-103">Ottiene una risorsa di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="a9d7c-103">Gets a private link resource.</span></span>

## <span data-ttu-id="a9d7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9d7c-104">SYNTAX</span></span>

### <span data-ttu-id="a9d7c-105">ByPrivateLinkResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9d7c-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9d7c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9d7c-106">DESCRIPTION</span></span>
<span data-ttu-id="a9d7c-107">Il cmdlet **Get-AzPrivateLinkResource** recupera tutte le risorse di collegamento appartiene PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="a9d7c-107">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="a9d7c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9d7c-108">EXAMPLES</span></span>

### <span data-ttu-id="a9d7c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a9d7c-109">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="a9d7c-110">Questo esempio elenca tutte le risorse del collegamento privato nbelong a SQL Server denominato mySql.</span><span class="sxs-lookup"><span data-stu-id="a9d7c-110">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="a9d7c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9d7c-111">PARAMETERS</span></span>

### <span data-ttu-id="a9d7c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d7c-112">-DefaultProfile</span></span>
<span data-ttu-id="a9d7c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d7c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9d7c-114">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a9d7c-114">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a9d7c-115">ID di gestione risorse di Azure della risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="a9d7c-115">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="a9d7c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d7c-116">CommonParameters</span></span>
<span data-ttu-id="a9d7c-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d7c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d7c-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9d7c-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d7c-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9d7c-119">INPUTS</span></span>

### <span data-ttu-id="a9d7c-120">System. String</span><span class="sxs-lookup"><span data-stu-id="a9d7c-120">System.String</span></span>

## <span data-ttu-id="a9d7c-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9d7c-121">OUTPUTS</span></span>

### <span data-ttu-id="a9d7c-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9d7c-122">System.Boolean</span></span>

## <span data-ttu-id="a9d7c-123">Note</span><span class="sxs-lookup"><span data-stu-id="a9d7c-123">NOTES</span></span>

## <span data-ttu-id="a9d7c-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9d7c-124">RELATED LINKS</span></span>
