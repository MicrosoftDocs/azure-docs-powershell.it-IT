---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023448"
---
# <span data-ttu-id="135ef-101">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="135ef-101">Remove-AzureVNetGateway</span></span>

## <span data-ttu-id="135ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="135ef-102">SYNOPSIS</span></span>
<span data-ttu-id="135ef-103">Elimina un gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="135ef-103">Deletes a VPN gateway.</span></span>

## <span data-ttu-id="135ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="135ef-104">SYNTAX</span></span>

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="135ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="135ef-105">DESCRIPTION</span></span>
<span data-ttu-id="135ef-106">Il cmdlet **Remove-AzureVNetGateway** Elimina un gateway VPN (Virtual Private Network) esistente per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="135ef-106">The **Remove-AzureVNetGateway** cmdlet deletes an existing virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="135ef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="135ef-107">EXAMPLES</span></span>

### <span data-ttu-id="135ef-108">Esempio 1: rimuovere un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="135ef-108">Example 1: Remove a virtual network gateway</span></span>
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="135ef-109">Questo comando rimuove il gateway di rete virtuale dalla rete virtuale denominata ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="135ef-109">This command removes the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="135ef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="135ef-110">PARAMETERS</span></span>

### <span data-ttu-id="135ef-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="135ef-111">-Profile</span></span>
<span data-ttu-id="135ef-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="135ef-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="135ef-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="135ef-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="135ef-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="135ef-114">-VNetName</span></span>
<span data-ttu-id="135ef-115">Specifica la rete virtuale in cui questo cmdlet elimina il gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="135ef-115">Specifies the virtual network in which this cmdlet deletes the VPN gateway.</span></span>

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

### <span data-ttu-id="135ef-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="135ef-116">CommonParameters</span></span>
<span data-ttu-id="135ef-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="135ef-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="135ef-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="135ef-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="135ef-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="135ef-119">INPUTS</span></span>

## <span data-ttu-id="135ef-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="135ef-120">OUTPUTS</span></span>

## <span data-ttu-id="135ef-121">Note</span><span class="sxs-lookup"><span data-stu-id="135ef-121">NOTES</span></span>

## <span data-ttu-id="135ef-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="135ef-122">RELATED LINKS</span></span>

[<span data-ttu-id="135ef-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="135ef-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="135ef-124">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="135ef-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="135ef-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="135ef-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="135ef-126">Ridimensionare-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="135ef-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="135ef-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="135ef-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


