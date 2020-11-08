---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029741"
---
# <span data-ttu-id="30532-101">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="30532-101">Get-AzureVNetGateway</span></span>

## <span data-ttu-id="30532-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30532-102">SYNOPSIS</span></span>
<span data-ttu-id="30532-103">Ottiene lo stato di un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="30532-103">Gets the status of a virtual network gateway.</span></span>

## <span data-ttu-id="30532-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30532-104">SYNTAX</span></span>

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30532-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30532-105">DESCRIPTION</span></span>
<span data-ttu-id="30532-106">Il cmdlet **Get-AzureVNetGateway** ottiene lo stato di un gateway di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="30532-106">The **Get-AzureVNetGateway** cmdlet gets the status of an existing virtual network gateway.</span></span>

## <span data-ttu-id="30532-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30532-107">EXAMPLES</span></span>

### <span data-ttu-id="30532-108">Esempio 1: ottenere lo stato di un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="30532-108">Example 1: Get the status of a virtual network gateway</span></span>
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="30532-109">Questo comando ottiene lo stato del gateway di rete virtuale per la rete virtuale denominato ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="30532-109">This command gets that status of the virtual network gateway for the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="30532-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30532-110">PARAMETERS</span></span>

### <span data-ttu-id="30532-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="30532-111">-Profile</span></span>
<span data-ttu-id="30532-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30532-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="30532-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="30532-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30532-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="30532-114">-VNetName</span></span>
<span data-ttu-id="30532-115">Specifica la rete virtuale che contiene il gateway di rete virtuale per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="30532-115">Specifies the virtual network that contains the virtual network gateway for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="30532-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30532-116">CommonParameters</span></span>
<span data-ttu-id="30532-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30532-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30532-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30532-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30532-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30532-119">INPUTS</span></span>

## <span data-ttu-id="30532-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30532-120">OUTPUTS</span></span>

## <span data-ttu-id="30532-121">Note</span><span class="sxs-lookup"><span data-stu-id="30532-121">NOTES</span></span>

## <span data-ttu-id="30532-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30532-122">RELATED LINKS</span></span>

[<span data-ttu-id="30532-123">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="30532-123">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="30532-124">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="30532-124">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="30532-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="30532-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="30532-126">Ridimensionare-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="30532-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="30532-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="30532-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


