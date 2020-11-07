---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: cc2ef6f016047bd20beba1671129a15c3dfa06f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855217"
---
# <span data-ttu-id="eb047-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb047-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="eb047-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb047-102">SYNOPSIS</span></span>
<span data-ttu-id="eb047-103">Aggiorna un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="eb047-103">Updates a public IP address.</span></span>

## <span data-ttu-id="eb047-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb047-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb047-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb047-105">DESCRIPTION</span></span>
<span data-ttu-id="eb047-106">Il cmdlet **set-AzPublicIpAddress** aggiorna un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="eb047-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="eb047-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb047-107">EXAMPLES</span></span>

### <span data-ttu-id="eb047-108">1: cambiare il metodo di assegnazione di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="eb047-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="eb047-109">Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="eb047-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="eb047-110">Secondo comando imposta il metodo di allocazione dell'oggetto indirizzo IP pubblico su "static".</span><span class="sxs-lookup"><span data-stu-id="eb047-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="eb047-111">Set-AzPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato e modifica il metodo di allocazione in "static".</span><span class="sxs-lookup"><span data-stu-id="eb047-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="eb047-112">Viene allocato immediatamente un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="eb047-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="eb047-113">2: modificare l'etichetta del dominio DNS di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="eb047-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="eb047-114">Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="eb047-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="eb047-115">Secondo comando imposta la proprietà DomainNameLabel sul prefisso DNS obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="eb047-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="eb047-116">Set-AzPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="eb047-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="eb047-117">DomainNameLabel & FQDN vengono modificati come previsto.</span><span class="sxs-lookup"><span data-stu-id="eb047-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="eb047-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb047-118">PARAMETERS</span></span>

### <span data-ttu-id="eb047-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb047-119">-AsJob</span></span>
<span data-ttu-id="eb047-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="eb047-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb047-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb047-121">-DefaultProfile</span></span>
<span data-ttu-id="eb047-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb047-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb047-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb047-123">-PublicIpAddress</span></span>
<span data-ttu-id="eb047-124">Specifica un oggetto indirizzo IP pubblico che rappresenta lo stato in cui deve essere impostato l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="eb047-124">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="eb047-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb047-125">CommonParameters</span></span>
<span data-ttu-id="eb047-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb047-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb047-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb047-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb047-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb047-128">INPUTS</span></span>

### <span data-ttu-id="eb047-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb047-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="eb047-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb047-130">OUTPUTS</span></span>

### <span data-ttu-id="eb047-131">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb047-131">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="eb047-132">Note</span><span class="sxs-lookup"><span data-stu-id="eb047-132">NOTES</span></span>

## <span data-ttu-id="eb047-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb047-133">RELATED LINKS</span></span>

[<span data-ttu-id="eb047-134">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb047-134">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="eb047-135">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb047-135">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="eb047-136">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb047-136">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


