---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B7E2561D-0FE8-4B34-9188-E89AA0B5C9DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: dce79fc891018c3100140581e89639dbc76b543d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029738"
---
# <span data-ttu-id="68402-101">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="68402-101">Get-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="68402-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68402-102">SYNOPSIS</span></span>
<span data-ttu-id="68402-103">Ottiene i parametri IPsec per la connessione tra un gateway di rete virtuale e un sito di rete locale.</span><span class="sxs-lookup"><span data-stu-id="68402-103">Gets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="68402-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68402-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="68402-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68402-105">DESCRIPTION</span></span>
<span data-ttu-id="68402-106">Il cmdlet **Get-AzureVNetGatewayIPsecParameters** restituisce i parametri IPSec (Internet Protocol Security) e Internet Key Exchange (IKE) correnti per la connessione tra un gateway di rete virtuale e un sito di rete locale.</span><span class="sxs-lookup"><span data-stu-id="68402-106">The **Get-AzureVNetGatewayIPsecParameters** cmdlet gets current Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="68402-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68402-107">EXAMPLES</span></span>

## <span data-ttu-id="68402-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68402-108">PARAMETERS</span></span>

### <span data-ttu-id="68402-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="68402-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="68402-110">Specifica il nome del sito di rete locale che si connette al gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="68402-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68402-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="68402-111">-Profile</span></span>
<span data-ttu-id="68402-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68402-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="68402-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="68402-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68402-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="68402-114">-VNetName</span></span>
<span data-ttu-id="68402-115">Specifica la rete virtuale per cui questo cmdlet ottiene i parametri IPsec per la connessione.</span><span class="sxs-lookup"><span data-stu-id="68402-115">Specifies the virtual network for which this cmdlet gets IPsec parameters for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68402-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68402-116">CommonParameters</span></span>
<span data-ttu-id="68402-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68402-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68402-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68402-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68402-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68402-119">INPUTS</span></span>

## <span data-ttu-id="68402-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68402-120">OUTPUTS</span></span>

## <span data-ttu-id="68402-121">Note</span><span class="sxs-lookup"><span data-stu-id="68402-121">NOTES</span></span>

## <span data-ttu-id="68402-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68402-122">RELATED LINKS</span></span>

[<span data-ttu-id="68402-123">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="68402-123">Set-AzureVNetGatewayIPsecParameters</span></span>](./Set-AzureVNetGatewayIPsecParameters.md)


