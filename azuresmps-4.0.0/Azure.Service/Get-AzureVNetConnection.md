---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7B749B29-9820-4E23-B5AF-F5535251629A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec94df29fb23dd7c82d79304c2e48aab225ed224
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029749"
---
# <span data-ttu-id="fdaba-101">Get-AzureVNetConnection</span><span class="sxs-lookup"><span data-stu-id="fdaba-101">Get-AzureVNetConnection</span></span>

## <span data-ttu-id="fdaba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdaba-102">SYNOPSIS</span></span>
<span data-ttu-id="fdaba-103">Ottiene connessioni a una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="fdaba-103">Gets connections to an Azure virtual network.</span></span>

## <span data-ttu-id="fdaba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdaba-104">SYNTAX</span></span>

```
Get-AzureVNetConnection -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fdaba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdaba-105">DESCRIPTION</span></span>
<span data-ttu-id="fdaba-106">Il cmdlet **Get-AzureVNetConnection** restituisce un oggetto che specifica tutte le connessioni VPN (Virtual Private Network) attive a una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="fdaba-106">The **Get-AzureVNetConnection** cmdlet returns an object that specifies all active virtual private network (VPN) connections to an Azure virtual network.</span></span>
<span data-ttu-id="fdaba-107">Le connessioni VPN includono le VPN da sito a sito e la rete virtuale per le connessioni di rete virtuali.</span><span class="sxs-lookup"><span data-stu-id="fdaba-107">VPN connections include cross premises site-to-site VPNs and virtual network to virtual network connections.</span></span>

## <span data-ttu-id="fdaba-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdaba-108">EXAMPLES</span></span>

## <span data-ttu-id="fdaba-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdaba-109">PARAMETERS</span></span>

### <span data-ttu-id="fdaba-110">-Profile</span><span class="sxs-lookup"><span data-stu-id="fdaba-110">-Profile</span></span>
<span data-ttu-id="fdaba-111">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdaba-111">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fdaba-112">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="fdaba-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fdaba-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="fdaba-113">-VNetName</span></span>
<span data-ttu-id="fdaba-114">Specifica il nome della rete virtuale da cui questo cmdlet restituisce le connessioni.</span><span class="sxs-lookup"><span data-stu-id="fdaba-114">Specifies the name of the virtual network from which this cmdlet returns connections.</span></span>

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

### <span data-ttu-id="fdaba-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdaba-115">CommonParameters</span></span>
<span data-ttu-id="fdaba-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdaba-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdaba-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdaba-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdaba-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdaba-118">INPUTS</span></span>

## <span data-ttu-id="fdaba-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdaba-119">OUTPUTS</span></span>

## <span data-ttu-id="fdaba-120">Note</span><span class="sxs-lookup"><span data-stu-id="fdaba-120">NOTES</span></span>

## <span data-ttu-id="fdaba-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdaba-121">RELATED LINKS</span></span>

