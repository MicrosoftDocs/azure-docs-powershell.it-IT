---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: 1460b4497909d56e2d10d03e33df71518c52b796
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685892"
---
# <span data-ttu-id="7f5a5-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f5a5-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="7f5a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f5a5-102">SYNOPSIS</span></span>
<span data-ttu-id="7f5a5-103">Imposta lo stato obiettivo per un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7f5a5-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f5a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f5a5-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f5a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f5a5-105">DESCRIPTION</span></span>
<span data-ttu-id="7f5a5-106">Il cmdlet **set-AzureRmPublicIpAddress** imposta lo stato dell'obiettivo per un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7f5a5-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="7f5a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f5a5-107">EXAMPLES</span></span>

### <span data-ttu-id="7f5a5-108">1: cambiare il metodo di assegnazione di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="7f5a5-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="7f5a5-109">Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="7f5a5-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="7f5a5-110">Secondo comando imposta il metodo di allocazione dell'oggetto indirizzo IP pubblico su "static".</span><span class="sxs-lookup"><span data-stu-id="7f5a5-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="7f5a5-111">Set-AzureRmPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato e modifica il metodo di allocazione in "static".</span><span class="sxs-lookup"><span data-stu-id="7f5a5-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="7f5a5-112">Viene allocato immediatamente un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7f5a5-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="7f5a5-113">2: modificare l'etichetta del dominio DNS di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="7f5a5-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="7f5a5-114">Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="7f5a5-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="7f5a5-115">Secondo comando imposta la proprietà DomainNameLabel sul prefisso DNS obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7f5a5-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="7f5a5-116">Set-AzureRmPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7f5a5-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="7f5a5-117">DomainNameLabel & FQDN vengono modificati come previsto.</span><span class="sxs-lookup"><span data-stu-id="7f5a5-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="7f5a5-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f5a5-118">PARAMETERS</span></span>

### <span data-ttu-id="7f5a5-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f5a5-119">-PublicIpAddress</span></span>
<span data-ttu-id="7f5a5-120">Specifica un oggetto **PublicIpAddress** che rappresenta lo stato dell'obiettivo a cui deve essere impostato l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7f5a5-120">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f5a5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f5a5-121">-DefaultProfile</span></span>
<span data-ttu-id="7f5a5-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f5a5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f5a5-123">CommonParameters</span></span>
<span data-ttu-id="7f5a5-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f5a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f5a5-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f5a5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f5a5-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f5a5-126">INPUTS</span></span>

### <span data-ttu-id="7f5a5-127">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f5a5-127">PSPublicIpAddress</span></span>
<span data-ttu-id="7f5a5-128">Il parametro ' PublicIpAddress ' accetta il valore di tipo ' PSPublicIpAddress ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7f5a5-128">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="7f5a5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f5a5-129">OUTPUTS</span></span>

### <span data-ttu-id="7f5a5-130">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f5a5-130">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7f5a5-131">Note</span><span class="sxs-lookup"><span data-stu-id="7f5a5-131">NOTES</span></span>

## <span data-ttu-id="7f5a5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f5a5-132">RELATED LINKS</span></span>

[<span data-ttu-id="7f5a5-133">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f5a5-133">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="7f5a5-134">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f5a5-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="7f5a5-135">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f5a5-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="7f5a5-136">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f5a5-136">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


