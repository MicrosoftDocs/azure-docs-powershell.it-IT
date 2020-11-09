---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311334"
---
# <span data-ttu-id="5247c-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5247c-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="5247c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5247c-102">SYNOPSIS</span></span>
<span data-ttu-id="5247c-103">Aggiorna un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="5247c-103">Updates a public IP address.</span></span>

## <span data-ttu-id="5247c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5247c-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5247c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5247c-105">DESCRIPTION</span></span>
<span data-ttu-id="5247c-106">Il cmdlet **set-AzPublicIpAddress** aggiorna un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="5247c-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="5247c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5247c-107">EXAMPLES</span></span>

### <span data-ttu-id="5247c-108">1: cambiare il metodo di assegnazione di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="5247c-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="5247c-109">Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="5247c-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="5247c-110">Secondo comando imposta il metodo di allocazione dell'oggetto indirizzo IP pubblico su "static".</span><span class="sxs-lookup"><span data-stu-id="5247c-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="5247c-111">Set-AzPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato e modifica il metodo di allocazione in "static".</span><span class="sxs-lookup"><span data-stu-id="5247c-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="5247c-112">Viene allocato immediatamente un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="5247c-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="5247c-113">2: aggiungere l'etichetta di dominio DNS di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="5247c-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="5247c-114">Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="5247c-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="5247c-115">Secondo comando imposta la proprietà DomainNameLabel sul prefisso DNS obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5247c-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="5247c-116">Set-AzPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5247c-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="5247c-117">DomainNameLabel & FQDN vengono modificati come previsto.</span><span class="sxs-lookup"><span data-stu-id="5247c-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="5247c-118">3: modificare l'etichetta del dominio DNS di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="5247c-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="5247c-119">Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="5247c-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="5247c-120">Secondo comando imposta la proprietà DomainNameLabel sul prefisso DNS obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5247c-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="5247c-121">Set-AzPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5247c-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="5247c-122">DomainNameLabel & FQDN vengono modificati come previsto.</span><span class="sxs-lookup"><span data-stu-id="5247c-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="5247c-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5247c-123">PARAMETERS</span></span>

### <span data-ttu-id="5247c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5247c-124">-AsJob</span></span>
<span data-ttu-id="5247c-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5247c-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5247c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5247c-126">-DefaultProfile</span></span>
<span data-ttu-id="5247c-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5247c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5247c-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5247c-128">-PublicIpAddress</span></span>
<span data-ttu-id="5247c-129">Specifica un oggetto indirizzo IP pubblico che rappresenta lo stato in cui deve essere impostato l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="5247c-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="5247c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5247c-130">CommonParameters</span></span>
<span data-ttu-id="5247c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5247c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5247c-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5247c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5247c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5247c-133">INPUTS</span></span>

### <span data-ttu-id="5247c-134">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5247c-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="5247c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5247c-135">OUTPUTS</span></span>

### <span data-ttu-id="5247c-136">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5247c-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="5247c-137">Note</span><span class="sxs-lookup"><span data-stu-id="5247c-137">NOTES</span></span>

## <span data-ttu-id="5247c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5247c-138">RELATED LINKS</span></span>

[<span data-ttu-id="5247c-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5247c-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="5247c-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5247c-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="5247c-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5247c-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


