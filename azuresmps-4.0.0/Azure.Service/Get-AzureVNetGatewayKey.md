---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8AD101BA-9275-4B2B-BB31-99FC34B8D1E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ac1d91bc084c9e1b17debf154b2a44c144ce312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029737"
---
# <span data-ttu-id="50a28-101">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="50a28-101">Get-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="50a28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50a28-102">SYNOPSIS</span></span>
<span data-ttu-id="50a28-103">Ottiene la chiave già condivisa per la connessione tra un gateway di rete virtuale e un sito di rete locale.</span><span class="sxs-lookup"><span data-stu-id="50a28-103">Gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="50a28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50a28-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="50a28-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50a28-105">DESCRIPTION</span></span>
<span data-ttu-id="50a28-106">Il cmdlet **Get-AzureVNetGatewayKey** ottiene la chiave già condivisa per la connessione tra un gateway di rete virtuale e un sito di rete locale.</span><span class="sxs-lookup"><span data-stu-id="50a28-106">The **Get-AzureVNetGatewayKey** cmdlet gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="50a28-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50a28-107">EXAMPLES</span></span>

## <span data-ttu-id="50a28-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50a28-108">PARAMETERS</span></span>

### <span data-ttu-id="50a28-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="50a28-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="50a28-110">Specifica il nome del sito di rete locale che si connette al gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="50a28-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="50a28-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="50a28-111">-Profile</span></span>
<span data-ttu-id="50a28-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50a28-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="50a28-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="50a28-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50a28-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="50a28-114">-VNetName</span></span>
<span data-ttu-id="50a28-115">Specifica la rete virtuale per cui questo cmdlet ottiene la chiave condivisa per le connessioni.</span><span class="sxs-lookup"><span data-stu-id="50a28-115">Specifies the virtual network for which this cmdlet gets the shared key for connections.</span></span>

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

### <span data-ttu-id="50a28-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a28-116">CommonParameters</span></span>
<span data-ttu-id="50a28-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50a28-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a28-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50a28-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a28-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50a28-119">INPUTS</span></span>

## <span data-ttu-id="50a28-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50a28-120">OUTPUTS</span></span>

## <span data-ttu-id="50a28-121">Note</span><span class="sxs-lookup"><span data-stu-id="50a28-121">NOTES</span></span>

## <span data-ttu-id="50a28-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50a28-122">RELATED LINKS</span></span>

[<span data-ttu-id="50a28-123">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="50a28-123">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


