---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: 61547a4ee5f60fccc371ca7b2c426ca1a4bbb005
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860926"
---
# <span data-ttu-id="027ae-101">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="027ae-101">Get-AzApplicationGateway</span></span>

## <span data-ttu-id="027ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="027ae-102">SYNOPSIS</span></span>
<span data-ttu-id="027ae-103">Ottiene un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="027ae-103">Gets an application gateway.</span></span>

## <span data-ttu-id="027ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="027ae-104">SYNTAX</span></span>

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="027ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="027ae-105">DESCRIPTION</span></span>
<span data-ttu-id="027ae-106">Il cmdlet **Get-AzApplicationGateway** ottiene un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="027ae-106">The **Get-AzApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="027ae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="027ae-107">EXAMPLES</span></span>

### <span data-ttu-id="027ae-108">Esempio 1: ottenere un gateway di applicazione specificato</span><span class="sxs-lookup"><span data-stu-id="027ae-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="027ae-109">Questo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="027ae-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="027ae-110">Esempio 2: ottenere un elenco dei gateway delle applicazioni in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="027ae-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="027ae-111">Questo comando consente di ottenere un elenco di tutti i gateway delle applicazioni nel gruppo di risorse denominato ResourceGroup01 e di archiviarlo nella variabile $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="027ae-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="027ae-112">Esempio 3: ottenere un elenco dei gateway delle applicazioni in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="027ae-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway
```

<span data-ttu-id="027ae-113">Questo comando ottiene un elenco di tutti i gateway dell'applicazione nell'abbonamento e lo archivia nella variabile $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="027ae-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="027ae-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="027ae-114">PARAMETERS</span></span>

### <span data-ttu-id="027ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="027ae-115">-DefaultProfile</span></span>
<span data-ttu-id="027ae-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="027ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="027ae-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="027ae-117">-Name</span></span>
<span data-ttu-id="027ae-118">Specifica il nome del gateway dell'applicazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="027ae-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="027ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="027ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="027ae-120">Specifica il nome del gruppo di risorse che contiene il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="027ae-120">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="027ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="027ae-121">CommonParameters</span></span>
<span data-ttu-id="027ae-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="027ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="027ae-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="027ae-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="027ae-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="027ae-124">INPUTS</span></span>

### <span data-ttu-id="027ae-125">System. String</span><span class="sxs-lookup"><span data-stu-id="027ae-125">System.String</span></span>

## <span data-ttu-id="027ae-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="027ae-126">OUTPUTS</span></span>

### <span data-ttu-id="027ae-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="027ae-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="027ae-128">Note</span><span class="sxs-lookup"><span data-stu-id="027ae-128">NOTES</span></span>

## <span data-ttu-id="027ae-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="027ae-129">RELATED LINKS</span></span>

[<span data-ttu-id="027ae-130">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="027ae-130">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


