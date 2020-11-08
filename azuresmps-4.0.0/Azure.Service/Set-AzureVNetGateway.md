---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029876"
---
# <span data-ttu-id="1005a-101">Set-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1005a-101">Set-AzureVNetGateway</span></span>

## <span data-ttu-id="1005a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1005a-102">SYNOPSIS</span></span>
<span data-ttu-id="1005a-103">Abilita o Disabilita un gateway VPN per una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="1005a-103">Enables or disables a VPN gateway for an Azure virtual network.</span></span>

## <span data-ttu-id="1005a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1005a-104">SYNTAX</span></span>

### <span data-ttu-id="1005a-105">Connect (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1005a-105">Connect (Default)</span></span>
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="1005a-106">Disconnettere</span><span class="sxs-lookup"><span data-stu-id="1005a-106">Disconnect</span></span>
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1005a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1005a-107">DESCRIPTION</span></span>
<span data-ttu-id="1005a-108">Il cmdlet **set-AzureVNetGateway** Abilita o Disabilita un gateway VPN (Virtual Private Network) per una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="1005a-108">The **Set-AzureVNetGateway** cmdlet enables or disables a virtual private network (VPN) gateway for an Azure virtual network.</span></span>
<span data-ttu-id="1005a-109">Un gateway di rete virtuale è un endpoint VPN per la connessione a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1005a-109">A virtual network gateway is a VPN endpoint for connecting to a virtual network.</span></span>
<span data-ttu-id="1005a-110">Specificare il parametro *Connect* o *Disconnect* per abilitare o disabilitare la connessione VPN tra un sito di rete locale e una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1005a-110">Specify the *Connect* or *Disconnect* parameter to enable or disable the VPN connection between an on-premises local network site and a virtual network.</span></span>

## <span data-ttu-id="1005a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1005a-111">EXAMPLES</span></span>

### <span data-ttu-id="1005a-112">Esempio 1: abilitare un gateway di rete virtuale per una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="1005a-112">Example 1: Enable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="1005a-113">Questo comando Abilita il gateway di rete virtuale tra la rete virtuale di Azure denominata ContosoProdNet e il dispositivo VPN per il sito di rete locale denominato ContosoBranchOffice.</span><span class="sxs-lookup"><span data-stu-id="1005a-113">This command enables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

### <span data-ttu-id="1005a-114">Esempio 2: disabilitare un gateway di rete virtuale per una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="1005a-114">Example 2: Disable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="1005a-115">Questo comando Disabilita il gateway di rete virtuale tra la rete virtuale di Azure denominata ContosoProdNet e il dispositivo VPN per il sito di rete locale denominato ContosoBranchOffice.</span><span class="sxs-lookup"><span data-stu-id="1005a-115">This command disables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

## <span data-ttu-id="1005a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1005a-116">PARAMETERS</span></span>

### <span data-ttu-id="1005a-117">-Connect</span><span class="sxs-lookup"><span data-stu-id="1005a-117">-Connect</span></span>
<span data-ttu-id="1005a-118">Indica che questo cmdlet Abilita la connessione VPN tra una rete virtuale e un sito di rete locale.</span><span class="sxs-lookup"><span data-stu-id="1005a-118">Indicates that this cmdlet enables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1005a-119">-Disconnetti</span><span class="sxs-lookup"><span data-stu-id="1005a-119">-Disconnect</span></span>
<span data-ttu-id="1005a-120">Indica che questo cmdlet disabilita la connessione VPN tra una rete virtuale e un sito di rete locale.</span><span class="sxs-lookup"><span data-stu-id="1005a-120">Indicates that this cmdlet disables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1005a-121">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="1005a-121">-LocalNetworkSiteName</span></span>
<span data-ttu-id="1005a-122">Specifica il nome del sito di rete locale locali per cui questo cmdlet Abilita o Disabilita la connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="1005a-122">Specifies the name of the on-premises local network site for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="1005a-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="1005a-123">-Profile</span></span>
<span data-ttu-id="1005a-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1005a-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1005a-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1005a-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1005a-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="1005a-126">-VNetName</span></span>
<span data-ttu-id="1005a-127">Specifica la rete virtuale per cui questo cmdlet Abilita o Disabilita la connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="1005a-127">Specifies the virtual network for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="1005a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1005a-128">CommonParameters</span></span>
<span data-ttu-id="1005a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1005a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1005a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1005a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1005a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1005a-131">INPUTS</span></span>

## <span data-ttu-id="1005a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1005a-132">OUTPUTS</span></span>

## <span data-ttu-id="1005a-133">Note</span><span class="sxs-lookup"><span data-stu-id="1005a-133">NOTES</span></span>

## <span data-ttu-id="1005a-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1005a-134">RELATED LINKS</span></span>

[<span data-ttu-id="1005a-135">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1005a-135">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="1005a-136">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1005a-136">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="1005a-137">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1005a-137">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="1005a-138">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1005a-138">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="1005a-139">Ridimensionare-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1005a-139">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)


