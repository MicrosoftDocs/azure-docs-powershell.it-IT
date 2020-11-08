---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023768"
---
# <span data-ttu-id="e92b8-101">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e92b8-101">Set-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="e92b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e92b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e92b8-103">Imposta la chiave già condivisa per la connessione tra un gateway di Azure VPN e un sito di rete locale.</span><span class="sxs-lookup"><span data-stu-id="e92b8-103">Sets the pre-shared key for the connection between an Azure VPN gateway and a local network site.</span></span>

## <span data-ttu-id="e92b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e92b8-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e92b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e92b8-105">DESCRIPTION</span></span>
<span data-ttu-id="e92b8-106">Il cmdlet **set-AzureVNetGatewayKey** imposta la chiave già condivisa per la connessione tra un gateway VPN (Virtual Private Network) di Azure e un sito di rete locale.</span><span class="sxs-lookup"><span data-stu-id="e92b8-106">The **Set-AzureVNetGatewayKey** cmdlet sets the pre-shared key for the connection between an Azure virtual private network (VPN) gateway and an on-premises local network site.</span></span>
<span data-ttu-id="e92b8-107">La chiave deve essere uguale alla chiave configurata nel gateway del sito di rete locale.</span><span class="sxs-lookup"><span data-stu-id="e92b8-107">The key must be equal to the key configured on the gateway of the local network site.</span></span>
<span data-ttu-id="e92b8-108">Se i tasti non corrispondono, non è possibile stabilire una connessione.</span><span class="sxs-lookup"><span data-stu-id="e92b8-108">If the keys do not match, a connection cannot establish.</span></span>

## <span data-ttu-id="e92b8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e92b8-109">EXAMPLES</span></span>

## <span data-ttu-id="e92b8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e92b8-110">PARAMETERS</span></span>

### <span data-ttu-id="e92b8-111">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="e92b8-111">-LocalNetworkSiteName</span></span>
<span data-ttu-id="e92b8-112">Specifica il nome del sito di rete locale che si connette al gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e92b8-112">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="e92b8-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="e92b8-113">-Profile</span></span>
<span data-ttu-id="e92b8-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e92b8-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e92b8-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e92b8-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e92b8-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="e92b8-116">-SharedKey</span></span>
<span data-ttu-id="e92b8-117">Specifica la chiave condivisa da assegnare al gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="e92b8-117">Specifies the shared key to assign to the VPN gateway.</span></span>
<span data-ttu-id="e92b8-118">Il valore deve essere una stringa alfa-numerica non più di 128 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e92b8-118">The value must be an alpha-numerical string no longer than 128 characters.</span></span>

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

### <span data-ttu-id="e92b8-119">-VNetName</span><span class="sxs-lookup"><span data-stu-id="e92b8-119">-VNetName</span></span>
<span data-ttu-id="e92b8-120">Specifica la rete virtuale per cui questo cmdlet imposta la chiave condivisa per la connessione.</span><span class="sxs-lookup"><span data-stu-id="e92b8-120">Specifies the virtual network for which this cmdlet sets the shared key for the connection.</span></span>

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

### <span data-ttu-id="e92b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e92b8-121">CommonParameters</span></span>
<span data-ttu-id="e92b8-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e92b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e92b8-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e92b8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e92b8-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e92b8-124">INPUTS</span></span>

## <span data-ttu-id="e92b8-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e92b8-125">OUTPUTS</span></span>

## <span data-ttu-id="e92b8-126">Note</span><span class="sxs-lookup"><span data-stu-id="e92b8-126">NOTES</span></span>

## <span data-ttu-id="e92b8-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e92b8-127">RELATED LINKS</span></span>

[<span data-ttu-id="e92b8-128">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e92b8-128">Get-AzureVNetGatewayKey</span></span>](./Get-AzureVNetGatewayKey.md)


