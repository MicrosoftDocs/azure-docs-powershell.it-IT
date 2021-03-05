---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 808a9f8d5ee4b15885e06e2ab4ac1fc7c5d1bed9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004941"
---
# <span data-ttu-id="c0f32-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="c0f32-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="c0f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0f32-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f32-103">Ottiene i codici di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c0f32-103">Gets subscription keys.</span></span>

## <span data-ttu-id="c0f32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0f32-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0f32-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c0f32-105">DESCRIPTION</span></span>
<span data-ttu-id="c0f32-106">Il cmdlet **Get-AzApiManagementSubscriptionKey** ottiene le chiavi di una sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c0f32-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="c0f32-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0f32-107">EXAMPLES</span></span>

### <span data-ttu-id="c0f32-108">Esempio 1: Ottenere una chiave di abbonamento con un ID specificato</span><span class="sxs-lookup"><span data-stu-id="c0f32-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="c0f32-109">Questo comando ottiene una sottoscrizione in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="c0f32-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="c0f32-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0f32-110">PARAMETERS</span></span>

### <span data-ttu-id="c0f32-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c0f32-111">-Context</span></span>
<span data-ttu-id="c0f32-112">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="c0f32-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0f32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f32-113">-DefaultProfile</span></span>
<span data-ttu-id="c0f32-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0f32-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0f32-115">-SubscriptionId</span></span>
<span data-ttu-id="c0f32-116">Specifica un identificatore di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c0f32-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="c0f32-117">Se specificato, questo cmdlet trova la sottoscrizione in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="c0f32-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0f32-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f32-118">CommonParameters</span></span>
<span data-ttu-id="c0f32-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f32-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f32-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c0f32-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f32-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="c0f32-121">INPUTS</span></span>

### <span data-ttu-id="c0f32-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c0f32-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c0f32-123">System.String</span><span class="sxs-lookup"><span data-stu-id="c0f32-123">System.String</span></span>

## <span data-ttu-id="c0f32-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0f32-124">OUTPUTS</span></span>

### <span data-ttu-id="c0f32-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="c0f32-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="c0f32-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="c0f32-126">NOTES</span></span>

## <span data-ttu-id="c0f32-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0f32-127">RELATED LINKS</span></span>

[<span data-ttu-id="c0f32-128">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c0f32-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="c0f32-129">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c0f32-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="c0f32-130">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c0f32-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="c0f32-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c0f32-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


