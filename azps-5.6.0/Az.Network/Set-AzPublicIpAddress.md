---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 33712b9813d6c23ed72097597d94a22bf7644992
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990946"
---
# <span data-ttu-id="222c2-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="222c2-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="222c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="222c2-102">SYNOPSIS</span></span>
<span data-ttu-id="222c2-103">Aggiorna un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="222c2-103">Updates a public IP address.</span></span>

## <span data-ttu-id="222c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="222c2-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="222c2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="222c2-105">DESCRIPTION</span></span>
<span data-ttu-id="222c2-106">Il **cmdlet Set-AzPublicIpAddress** aggiorna un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="222c2-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="222c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="222c2-107">EXAMPLES</span></span>

### <span data-ttu-id="222c2-108">1: modificare il metodo di assegnazione di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="222c2-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="222c2-109">Il primo comando ottiene la risorsa indirizzo IP pubblico con nome $publicIPName nel gruppo di $rgName.</span><span class="sxs-lookup"><span data-stu-id="222c2-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="222c2-110">Il secondo comando imposta il metodo di allocazione dell'oggetto indirizzo IP pubblico su "Statico".</span><span class="sxs-lookup"><span data-stu-id="222c2-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="222c2-111">Set-AzPublicIPAddress aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato e modifica il metodo di assegnazione in "Statico".</span><span class="sxs-lookup"><span data-stu-id="222c2-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="222c2-112">Un indirizzo IP pubblico viene allocato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="222c2-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="222c2-113">2: Aggiungere l'etichetta di dominio DNS di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="222c2-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="222c2-114">Il primo comando ottiene la risorsa indirizzo IP pubblico con nome $publicIPName nel gruppo di $rgName.</span><span class="sxs-lookup"><span data-stu-id="222c2-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="222c2-115">Il secondo comando imposta la proprietà DomainNameLabel sul prefisso DNS obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="222c2-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="222c2-116">Set-AzPublicIPAddress comando aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="222c2-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="222c2-117">DomainNameLabel & fqdn vengono modificati nel modo previsto.</span><span class="sxs-lookup"><span data-stu-id="222c2-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="222c2-118">3: Modificare l'etichetta del dominio DNS di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="222c2-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="222c2-119">Il primo comando ottiene la risorsa indirizzo IP pubblico con nome $publicIPName nel gruppo di $rgName.</span><span class="sxs-lookup"><span data-stu-id="222c2-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="222c2-120">Il secondo comando imposta la proprietà DomainNameLabel sul prefisso DNS obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="222c2-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="222c2-121">Set-AzPublicIPAddress comando aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="222c2-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="222c2-122">DomainNameLabel & fqdn vengono modificati nel modo previsto.</span><span class="sxs-lookup"><span data-stu-id="222c2-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="222c2-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="222c2-123">PARAMETERS</span></span>

### <span data-ttu-id="222c2-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="222c2-124">-AsJob</span></span>
<span data-ttu-id="222c2-125">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="222c2-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="222c2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="222c2-126">-DefaultProfile</span></span>
<span data-ttu-id="222c2-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="222c2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="222c2-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="222c2-128">-PublicIpAddress</span></span>
<span data-ttu-id="222c2-129">Specifica un oggetto indirizzo IP pubblico che rappresenta lo stato su cui deve essere impostato l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="222c2-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="222c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="222c2-130">CommonParameters</span></span>
<span data-ttu-id="222c2-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="222c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="222c2-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="222c2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="222c2-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="222c2-133">INPUTS</span></span>

### <span data-ttu-id="222c2-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="222c2-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="222c2-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="222c2-135">OUTPUTS</span></span>

### <span data-ttu-id="222c2-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="222c2-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="222c2-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="222c2-137">NOTES</span></span>

## <span data-ttu-id="222c2-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="222c2-138">RELATED LINKS</span></span>

[<span data-ttu-id="222c2-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="222c2-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="222c2-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="222c2-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="222c2-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="222c2-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


