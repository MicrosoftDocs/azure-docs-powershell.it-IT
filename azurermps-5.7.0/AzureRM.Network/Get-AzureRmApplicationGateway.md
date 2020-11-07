---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
ms.openlocfilehash: 2c49a71521e40cbe9e42c1a06c5c3d785a74d52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686198"
---
# <span data-ttu-id="3477f-101">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3477f-101">Get-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="3477f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3477f-102">SYNOPSIS</span></span>
<span data-ttu-id="3477f-103">Ottiene un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3477f-103">Gets an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3477f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3477f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3477f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3477f-105">DESCRIPTION</span></span>
<span data-ttu-id="3477f-106">Il cmdlet **Get-AzureRmApplicationGateway** ottiene un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3477f-106">The **Get-AzureRmApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="3477f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3477f-107">EXAMPLES</span></span>

### <span data-ttu-id="3477f-108">Esempio 1: ottenere un gateway di applicazione specificato</span><span class="sxs-lookup"><span data-stu-id="3477f-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3477f-109">Questo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3477f-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="3477f-110">Esempio 2: ottenere un elenco dei gateway delle applicazioni in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3477f-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3477f-111">Questo comando consente di ottenere un elenco di tutti i gateway delle applicazioni nel gruppo di risorse denominato ResourceGroup01 e di archiviarlo nella variabile $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="3477f-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="3477f-112">Esempio 3: ottenere un elenco dei gateway delle applicazioni in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="3477f-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

<span data-ttu-id="3477f-113">Questo comando ottiene un elenco di tutti i gateway dell'applicazione nell'abbonamento e lo archivia nella variabile $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="3477f-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="3477f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3477f-114">PARAMETERS</span></span>

### <span data-ttu-id="3477f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3477f-115">-DefaultProfile</span></span>
<span data-ttu-id="3477f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3477f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3477f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3477f-117">-Name</span></span>
<span data-ttu-id="3477f-118">Specifica il nome del gateway dell'applicazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3477f-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3477f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3477f-119">-ResourceGroupName</span></span>
<span data-ttu-id="3477f-120">Specifica il nome del gruppo di risorse che contiene il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3477f-120">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3477f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3477f-121">CommonParameters</span></span>
<span data-ttu-id="3477f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3477f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3477f-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3477f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3477f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3477f-124">INPUTS</span></span>

### <span data-ttu-id="3477f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3477f-125">System.String</span></span>

## <span data-ttu-id="3477f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3477f-126">OUTPUTS</span></span>

### <span data-ttu-id="3477f-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3477f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3477f-128">Note</span><span class="sxs-lookup"><span data-stu-id="3477f-128">NOTES</span></span>

## <span data-ttu-id="3477f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3477f-129">RELATED LINKS</span></span>

[<span data-ttu-id="3477f-130">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3477f-130">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


